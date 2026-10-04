# GPU Communication Boundaries

**Context:** Independent AI infrastructure research<br>
**Status:** Completed intra-node investigation; cross-node work deferred<br>
**Domain:** GPU placement, NUMA/PCIe topology, NCCL transport selection, collective and application performance<br>
**Repository:** [View the public case-study repository on GitHub](https://github.com/Robert-N-Myhre/gpu-communication-boundaries-case-study)

## Overview

I investigated whether crossing a CPU socket boundary imposed a measurable performance cost on GPU communication, and whether collective benchmark differences carried through to a distributed training workload.

The study used a four-V100 PCIe workstation and a rented four-L40S cloud instance. The initial expectation was that crossing the socket boundary would be expensive. Controlled comparisons showed that placement alone did not explain the results: the communication mechanism selected by NCCL mattered more, and its benchmark performance did not reliably predict application throughput.

## Objective

Separate three questions that a topology diagram alone cannot answer:

- What paths does the hardware support?
- Which transport does the runtime actually select?
- How much does that choice affect the application?

The comparisons varied GPU placement and transport policy within each platform. The two systems provided complementary experiments, rather than a controlled V100-versus-L40S ranking.

## Architecture and Method

The investigation combined topology and P2P capability captures, NCCL transport logs, repeated all-reduce benchmarks, and a 124-million-parameter PyTorch DDP training workload using synthetic tokens in fp32.

Runs were interleaved across configurations, with medians, observed spreads, host state, and GPU telemetry retained. Application transport captures were checked separately because PyTorch bundled a different NCCL version.

Two discoveries on the L40S instance required revising the experiment: the default four-GPU ring used host staging, while default two-GPU jobs used P2P. Planned policy contrasts therefore had to be checked against the selected transport before their performance could be interpreted.

## Selected Findings

### Placement and mechanism required separate controls

Under matched transports, crossing the socket boundary produced no measurable collective penalty in the tested comparisons.

Changing the mechanism did affect bandwidth: forcing P2P improved the V100 same-socket pair by approximately 15%; disabling P2P reduced L40S pair bandwidth by approximately 18% at both placements.

### Capability did not establish runtime selection

NCCL selected host staging on paths where P2P was available. On the tested L40S instance, default selection also changed with communicator size.

A supported hardware path and a configured policy were insufficient evidence of the path used by a particular job.

### Faster collectives did not guarantee faster training

The mixed-transport rings underperformed the all-host-staged rings by approximately 10% on V100 and 37% on L40S.

Application effects were much smaller. The L40S same-NUMA pair's approximately 18% collective-bandwidth loss accompanied a training-throughput difference within the observed spread. Some collective improvements accompanied application regressions.

## Architectural Finding

Before paying for topology-aware placement or forcing a transport policy, verify the selected mechanism and measure whether the workload benefits.

The transferable result is the measurement approach: distinguish hardware capability, runtime behavior, and application impact; revise comparisons when observations contradict their assumptions; and retain unresolved causes as open questions.

## Scope and Evidence

These findings describe one workstation, one cloud instance, and one synthetic training workload. Observed spreads are descriptive comparisons, not statistical equivalence tests. Cross-node communication, NVLink, RDMA, and network fabrics were not tested.

The accumulation experiment improved throughput, but also changed optimizer-update frequency; it did not isolate communication time.

The public repository contains the full case study, selected evidence, platform qualification methodology, two decision records, a transport-discovery field note, and five unchanged research instruments. The complete run archive and provisioning toolkit are not published.

[Read the full case study →](https://github.com/Robert-N-Myhre/gpu-communication-boundaries-case-study/blob/main/gpu-communication-boundaries-case-study.md) · [Inspect the supporting evidence →](https://github.com/Robert-N-Myhre/gpu-communication-boundaries-case-study/blob/main/evidence/README.md)
