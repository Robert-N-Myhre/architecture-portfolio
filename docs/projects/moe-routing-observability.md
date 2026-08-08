# MoE Routing Observability

**Context:** Independent AI infrastructure research  
**Status:** Completed research series  
**Domain:** Multi-GPU inference, Mixture of Experts, observability, NUMA/PCIe topology, model placement  
**Repository:** [View the public research repository on GitHub](https://github.com/Robert-N-Myhre/moe-routing-observability)

## Overview

I instrumented Mixture-of-Experts (MoE) inference on a four-GPU NVIDIA V100 server to understand what sparse models actually demand from constrained infrastructure.

The investigation focused less on model quality than on infrastructure behavior: router decisions, expert placement, memory requirements, PCIe and NUMA traffic, runtime compatibility, and whether commonly reported performance measurements were actually telling the full story.

Several initial assumptions did not survive measurement.

## Objective

Make MoE inference observable enough to answer infrastructure questions that aggregate throughput alone cannot:

- How does expert routing affect device and interconnect behavior?
- What does model placement cost across NUMA boundaries?
- Does successful quantized loading prove that the expert weights were actually quantized?
- Can runtime configuration be trusted simply because an API accepts and reports it?
- How much of an apparent performance difference survives repeated trials and better controls?
- What infrastructure burden remains even when only a subset of experts is active for each token?

The goal was not to optimize a benchmark score. It was to understand which measurements are required before drawing architecture conclusions from MoE workloads.

## Architecture and Method

The primary platform was a dual-NUMA server with four NVIDIA V100 16 GB GPUs connected through PCIe without NVLink.

Experiments used controlled model placement, router-logit capture, GPU and PCIe telemetry, per-parameter dtype inspection, repeated benchmark trials, and explicit evidence records.

The research was structured so that claims remained tied to captured evidence and corrections remained visible when later experiments invalidated an earlier conclusion.

## Selected Findings

### Placement costs can be invisible to throughput

Cross-NUMA expert dispatch produced substantially higher PCIe traffic than same-NUMA dispatch in the tested runs, while aggregate token throughput remained effectively unchanged.

The important result was not that one placement was universally slower. It was that a throughput-only view would have hidden a large difference in interconnect behavior.

### Successful model loading did not prove quantization succeeded

A MoE model requested with quantization could load successfully while large portions of the expert pool remained unquantized.

This demonstrated that configuration intent and successful startup were insufficient validation. Per-parameter inspection was required to determine what actually happened.

### Accepted configuration did not prove runtime behavior

A vLLM expert-placement configuration was accepted and reflected through the configuration interface, but later validation showed that the requested placement policy had not actually taken effect.

Repeated trials also disproved an apparent performance improvement that had initially looked significant.

### Better controls changed conclusions

NUMA pinning and repeated measurements exposed confounding factors in earlier experiments.

Rather than preserve the original findings, the research record retains the corrections and documents why the conclusions changed.

## Architectural Finding

MoE reduces active computation per token, but it does not eliminate the infrastructure burden of placing and operating the full model.

Sparse routing also introduces behavior that can remain invisible when infrastructure is evaluated only through aggregate application metrics.

For architecture and operations, meaningful MoE observability therefore needs to include more than tokens per second. It can require visibility into:

- router behavior
- model and expert placement
- actual parameter dtypes
- GPU memory pressure
- NUMA locality
- PCIe traffic
- runtime compatibility
- repeated-trial variance

The specific measurements in this project are constrained to the tested hardware. The instrumentation and validation approach are the more transferable result.

## What This Demonstrates

This research demonstrates an evidence-driven approach to AI infrastructure.

The useful findings included both expected behavior and negative results: configurations that silently failed, conclusions that reversed under better controls, performance differences that disappeared under repeated trials, and infrastructure costs that application-level metrics did not expose.

The public repository contains the methodology, findings, lab guides, instrumentation scripts, captured results, reproduction guidance, and provenance describing how AI assistance was used during the research.

[Explore the full MoE Routing Observability research →](https://github.com/Robert-N-Myhre/moe-routing-observability)