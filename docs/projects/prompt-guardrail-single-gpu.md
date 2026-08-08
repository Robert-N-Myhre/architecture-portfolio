# Prompt Security Guardrails on a Single GPU

**Context:** Independent AI infrastructure and safety research<br>
**Status:** Completed research series; conditional architecture decision<br>
**Domain:** AI guardrails, GPU co-residency, deterministic orchestration, prompt injection, inference resource constraints<br>
**Repository:** [View the public research repository on GitHub](https://github.com/Robert-N-Myhre/Prompt-guardrail-single-gpu)

## Overview

I tested whether a security-specialized language model could operate as a local prompt-risk guard for a co-resident reasoning model on a single 20 GB GPU.

The hardware constraint was deliberate. The investigation was not simply about whether two models could fit into VRAM. It examined whether both models could remain resident, whether guardrail latency was operationally tolerable, whether parallel inference improved throughput, and whether model-based safety decisions were reliable enough to control progression through the workflow.

The answer was conditional.

The models could remain co-resident with usable memory headroom, but inference needed to remain sequential. More importantly, the safety architecture became credible only after deterministic controls were placed around the model judgments.

## Objective

Determine whether a constrained single-GPU platform could support:

- a security-specialized guard model
- a separate reasoning model
- enough remaining VRAM for stable operation
- acceptable sequential guardrail overhead
- deterministic control over model-generated safety decisions
- prompt-injection resistance strong enough to justify continued use

The goal was to evaluate the architecture as a system rather than treat successful model loading or individual guard verdicts as sufficient evidence.

## Architecture and Method

The tested workflow used three model stages:

1. the guard model classified the incoming request
2. the reasoning model generated a proposed plan
3. the guard model reviewed that plan

Model outputs did not directly authorize progression.

Deterministic gates recomputed the guard's dispositions from structured evidence, and a deterministic plan scanner was added between plan generation and model review after testing exposed an injection path that the model-only review failed to stop.

Both models remained loaded on the same GPU, while the inference stages executed sequentially.

The research used scripted measurement and evidence capture for VRAM use, latency, throughput, guardrail scoring, contention behavior, and architecture validation.

## Selected Findings

### Co-residency was viable

The guard and reasoning models occupied approximately 16.6 GiB together on the tested 20 GB GPU, leaving roughly 3.9 GiB of measured headroom.

Repeated labs reproduced the model residency footprint closely enough to support co-residency as an architecture option on the tested platform.

### Parallel inference did not improve throughput

Running the two model processes concurrently did not produce useful GPU co-execution in the tested configuration.

Measured pipelining was slightly slower than sequential execution, indicating time-slicing rather than beneficial parallel inference.

Sequential execution therefore became an explicit architecture constraint rather than an assumed limitation.

### Model verdicts required deterministic enforcement

The initial guard contract produced dangerous effective false approvals in the evaluation battery.

Recomputing the model's structured verdict through deterministic orchestration reduced those effective false approvals from six to zero across the tested 19-case battery.

The result did not prove that the guard model was universally safe. It demonstrated that model judgment became more useful when authority remained outside the model.

### One successful injection exposed a missing control

A prompt-injection scenario passed the initial triage stage and was rationalized by the later model review.

That failure occurred at a point where no deterministic backstop existed.

A deterministic plan scanner was added at that boundary and subsequently caught both replayed injected plans in the validation run with sub-millisecond execution time.

## Architectural Finding

The central result was not that a security model could reliably act as an autonomous guard.

It could not.

The more defensible architecture treated the model as a **noisy witness** whose judgments informed deterministic controls.

Authority remained with the orchestrator.

This created a clearer separation between:

- probabilistic model judgment
- structured evidence
- deterministic policy enforcement
- human escalation
- controlled progression toward execution

The GPU constraint also mattered operationally. Co-residency avoided repeated model loading, but sequential inference imposed a measurable latency cost and constrained the latency and throughput envelope of this particular single-GPU design.

## Limits

The research provides existence proofs rather than production safety rates.

The evaluation battery contained 19 hand-written cases in one domain, the successful injection represented a specific attack pattern, and the deterministic scanner detects a bounded class of patterns rather than semantic intent.

The parallel-inference result is also specific to the tested runtime and two-process configuration without NVIDIA MPS.

The measurements should therefore be treated as evidence about the tested architecture, not universal performance or security claims.

## What This Demonstrates

This project combined AI infrastructure constraints with AI safety architecture.

It began as a resource-placement question and evolved into a broader control-plane finding: successful model deployment is not enough when model output can influence infrastructure actions.

The resulting architecture separates judgment from authority and uses deterministic controls to validate, constrain, or reject model decisions before progression.

Those findings became a precursor to later work on governed agentic infrastructure and controlled AI-assisted operations.

The public repository contains all nine lab guides, evidence files, findings, architecture decisions, measurement and analysis scripts, reproduction guidance, and provenance describing how AI assistance was used during the research.

[Explore the full Prompt Security Guardrails research →](https://github.com/Robert-N-Myhre/Prompt-guardrail-single-gpu)
