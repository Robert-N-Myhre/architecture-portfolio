# MCP Platform Case Study: Build, Validate, Reject

**Context:** Independent architecture research<br>
**Status:** Completed; platform development deliberately closed<br>
**Domain:** MCP infrastructure, identity, security boundaries, workload isolation, platform architecture<br>
**Repository:** [View the public case study on GitHub](https://github.com/Robert-N-Myhre/mcp-platform-case-study)

## Overview

I built and validated a centralized Model Context Protocol (MCP) service harness to test whether multiple MCP services could share a common access, execution, and security boundary without distributing service credentials to every client or exposing the services directly.

The implementation worked.

The reusable-platform hypothesis did not.

Rather than continue extending a technically functional design, I closed the project when the evidence showed that the abstraction was not reducing the cost or complexity of adding real services.

## Objective

Determine whether a centralized MCP platform could provide reusable infrastructure for:

- per-client access identity
- restricted MCP execution
- isolated and immutable workloads
- controlled network access
- credential containment
- lifecycle and drift management
- multiple MCP services behind a common platform boundary

The goal was not simply to make an MCP server work remotely. The architecture needed to make the **next service materially easier and safer to add**.

## Architecture and Validation

The platform used per-client SSH identities, a forced-command dispatcher, restricted privilege escalation, and ephemeral containerized MCP workloads.

Workloads were constrained through explicit execution and network boundaries, including destination-specific egress controls, immutable image pinning, supply-chain verification, session isolation, and reconciliation logic.

A NetBox MCP server became the first real service used to test whether the platform abstraction held.

End-to-end validation demonstrated:

- remote MCP access through the complete platform boundary
- successful read-only NetBox operations from a remote AI client
- concurrent session isolation
- workload cleanup after session completion
- restricted egress to the approved upstream service
- recovery across Docker and host restarts
- explicit handling of policy drift and unknown workload state

## Architectural Finding

NetBox exposed three weaknesses that the generic test workload had not:

1. **Service integration remained highly customized.**  
   Adding the first real MCP service still required substantial service-specific launch, lifecycle, installation, policy, credential, and validation work.

2. **Authentication did not become downstream authorization.**  
   The platform could identify the initiating client at the MCP access boundary, but that identity did not propagate into authorization at the upstream service.

3. **Marginal service cost remained too high.**  
   The platform was centralizing MCP services without abstracting enough of the work required to operate them.

The architecture therefore failed its most important test: the next real service was not becoming sufficiently easier to add.

## Outcome

Development of the custom host-based platform was deliberately stopped. The working NetBox MCP deployment was retained; what ended was continued development of the custom harness surrounding it.

The decision was not based on implementation failure. It was based on evidence that continuing would mean investing further in custom versions of capabilities increasingly resembling general orchestration primitives such as reconciliation, workload isolation, lifecycle management, recovery, and policy enforcement.

Several architectural principles survived the rejected implementation:

- per-client identity
- verified server and workload identity
- verified workload identity
- isolated and immutable workloads

Those principles, along with unresolved identity and authorization questions, became requirements for the next architecture rather than reasons to preserve the original implementation.

## What This Demonstrates

This project is an example of architecture as hypothesis testing rather than implementation completion.

The useful result was not simply that the system worked. It was determining where the design stopped providing enough architectural value to justify further investment.

The full public repository includes the decision records, validation findings, diagrams, implementation components, retrospective, and the transition into the next Kubernetes and IAM-focused investigation.

[Explore the full MCP Platform Case Study →](https://github.com/Robert-N-Myhre/mcp-platform-case-study)