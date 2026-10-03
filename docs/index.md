<div style="display: flex; justify-content: space-between; align-items: flex-start;">

<div style="line-height: 1.3; margin-top: 0;">
<div style="font-size: 2em; font-weight: 700; margin-bottom: 0.2em;">
  Robert N. Myhre, CCIE #9837 (Active)
</div>
  <p style="margin: 0;"><strong>Principal Infrastructure Architect | Cross-Domain Architecture & Technology Strategy</strong></p>
  <p style="margin: 0;">✉️ ccie9837@gmail.com</p>
  <p style="margin: 0;">🔗 <a href="https://www.linkedin.com/in/robert-n-myhre">LinkedIn</a></p>
</div>

<div>
  <img src="assets/images/ccie_20years_med.jpg" alt="CCIE Logo" style="width: 150px; margin-left: 20px;" />
</div>

</div>

---

# Architecture Portfolio

I’m a principal-level infrastructure architect with more than 25 years in enterprise technology and more than 15 years in architecture roles.

Networking is my deepest technical foundation, but my work spans enterprise infrastructure, cloud, security, platform engineering, infrastructure automation, AI infrastructure, and enterprise architecture. I focus on the dependencies between those domains: where they constrain one another, where architectural decisions propagate across boundaries, and how those interactions should shape technology strategy.

This portfolio captures that work through enterprise architecture decisions, reusable reference architectures, emerging-technology research, and hands-on validation. The common thread is architectural reasoning: identifying assumptions, testing constraints, separating architectural intent from implementation choices, and turning complex technology into patterns that organizations can actually build, operate, and govern.

---

## Selected Work

### Enterprise Architecture Decisions

Selected case studies focused on architectural tradeoffs, validation, and decisions made under real enterprise constraints.

- [Dual Data Center Architecture: Choosing the Right Fabric Model](projects/dc-aci-project.md)
- [Multi-Cloud Connectivity: Choosing a Network-as-a-Service Model](projects/multicloud-network-architecture.md)
- [Multi-Cloud Architecture: Preserving Patterns Without Forcing Symmetry](projects/multicloud-terraform.md)
- [Enterprise Segmentation Architecture: Evidence-Based Platform Evaluation](projects/sda-segmentation.md)

### Emerging Technology & AI Infrastructure

Architecture frameworks, hands-on research, and case studies used to test assumptions, measure behavior, and reason about where emerging infrastructure and AI designs succeed, fail, or encounter meaningful constraints.

- **[Intelligence Placement Under Constraint](projects/intelligence-placement-under-constraint.md)**
  A systems-architecture framework for reasoning about where enterprise AI capabilities should execute, how context and decisions flow across layers, and how latency, locality, governance, cost, failure, and trust shape placement.

- **[MCP Platform Case Study](projects/mcp-platform-case-study.md)**
  Built and validated a centralized MCP platform, then rejected the reusable-platform hypothesis when implementation evidence showed the abstraction was not reducing integration cost.

- **[MoE Routing Observability](projects/moe-routing-observability.md)**
  Multi-GPU investigation of mixture-of-experts routing, topology, communication behavior, and observability.

- **[Prompt Security Guardrails](projects/prompt-guardrail-single-gpu.md)**
  Experimental evaluation of guardrail and workload co-residency constraints on a single GPU.

---

## Reference Architectures

Reusable architecture patterns focused on governed automation, explicit authority boundaries, deterministic controls, and auditability.

- [Monitor → Classify → Escalate](reference-architectures/monitor-classify-escalate.md)
- [Plan → Approve → Execute → Verify](reference-architectures/plan-approve-execute-verify.md)

---

## Architecture Practice

My architecture work is grounded in a simple principle: emerging technology becomes useful only when its assumptions, constraints, operational boundaries, and failure modes are understood.

I use design, implementation, lab validation, measurement, and documented decisions to determine what is supportable, what needs to change, and sometimes what should not be built.

- [Architecture Practice & Leadership](portfolio/architecture-practice.md)
- [Architectural Philosophy](architectural-philosophy.md)

---

## About

More about my professional background, current architecture work, research, and how these areas fit together.

- [About Me](about.md)