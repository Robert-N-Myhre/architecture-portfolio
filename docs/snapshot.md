<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="line-height: 1.3; margin-top: 0; flex-grow: 1; flex-shrink: 1; flex-basis: 75%;">
    <h1 style="margin-bottom: 0.2em;">Robert N. Myhre, CCIE #9837 (Active)</h1>
    <p style="margin: 0 0 0.4em 0;"><strong>Principal Architect | AI Infrastructure, Networking & Automation</strong></p>
    <div style="font-size: 0.85em; line-height: 1.25; margin-left: 2em;">
      <p style="margin: 0;">📎 Portfolio: <a href="https://robert-n-myhre.github.io/architecture-portfolio">robert-n-myhre.github.io/architecture-portfolio</a></p>
      <p style="margin: 0;">✉️ ccie9837@gmail.com</p>
      <p style="margin: 0;">🔗 <a href="https://www.linkedin.com/in/robert-n-myhre">LinkedIn</a> · <a href="https://github.com/Robert-N-Myhre">GitHub</a></p>
    </div>
    <p style="margin: 0.8em 0 0.4em 0; font-style: italic; color: #555; white-space: nowrap; font-size: 0.95em;">
      Architecture isn’t just about what I design—it’s about what others can build on top of it.
    </p>
  </div>

  <div style="flex: 0 0 auto;">
    <img id="ccie-logo" src="../assets/images/ccie_20years_med.jpg" alt="CCIE Logo" style="width: 120px; margin-left: 20px;" />
  </div>
</div>

## Summary

Principal-level infrastructure architect and dual CCIE with more than 25 years in enterprise infrastructure, including more than 15 years in architecture roles spanning networking, data center, cloud, and security.

My foundation is deep enterprise networking and data center architecture. My current professional work increasingly intersects with AI infrastructure, while my independent research explores multi-GPU systems, high-performance networking, observability, governed agentic systems, MCP, and infrastructure automation.

I work between strategy and implementation: identifying the assumptions and constraints that matter, validating where necessary, and using evidence to determine what should be built, what should change, and sometimes what should be stopped.

---

## Selected AI Infrastructure & Agentic Systems Work

### [MCP Platform Case Study](projects/mcp-platform-case-study.md)

Built and validated a centralized MCP platform with constrained identity, execution, workload isolation, and network boundaries. The implementation worked, but evidence showed that the reusable-platform abstraction was not reducing the cost of adding real services, so further platform development was deliberately stopped.

### [MoE Routing Observability](projects/moe-routing-observability.md)

Instrumented multi-GPU Mixture-of-Experts inference to examine routing behavior, topology, NUMA/PCIe effects, model placement, quantization validation, and the limits of aggregate throughput as an infrastructure metric.

### [Prompt Security Guardrails](projects/prompt-guardrail-single-gpu.md)

Evaluated GPU co-residency and AI safety controls on a constrained single-GPU platform. The research demonstrated that model judgment alone was insufficient and that deterministic controls were required to keep authority outside the model.

---

## Enterprise Architecture Decisions

These case studies focus less on the products selected and more on the reasoning, tradeoffs, and evidence behind the architecture decisions.

### [Dual Data Center Architecture: Choosing the Right Fabric Model](projects/dc-aci-project.md)

Compared traditional data center architecture and multiple Cisco ACI deployment models. Multi-Pod repeatedly proved to be an effective balance of policy consistency, dual-site resiliency, and operational complexity in the environments where I applied the pattern.

### [Multi-Cloud Connectivity: Choosing a Network-as-a-Service Model](projects/multicloud-network-architecture.md)

Introduced a Network-as-a-Service abstraction to move cloud expansion away from repeated physical circuit procurement while balancing implementation speed, resiliency, operational complexity, and provider dependency.

### [Multi-Cloud Architecture: Preserving Patterns Without Forcing Symmetry](projects/multicloud-terraform.md)

Extended an established AWS operating model into Azure while preserving familiar hub-and-spoke, inspection, and Terraform patterns without forcing cloud constructs to be identical.

### [Enterprise Segmentation Architecture: Evidence-Based Platform Evaluation](projects/sda-segmentation.md)

Used explicit acceptance criteria, lab validation, automation, stakeholder review, and operational-readiness assessment to evaluate Cisco SDA. Better evidence changed the original recommendation, demonstrating that selection for validation is not selection for production.

---

## Reference Architectures

I also publish vendor-neutral architecture patterns for governed AI-assisted infrastructure operations.

### [Monitor → Classify → Escalate](reference-architectures/monitor-classify-escalate.md)

A pattern for AI-assisted event triage with structured outputs, deterministic confidence scoring, enrichment, human escalation, and complete auditability.

### [Plan → Approve → Execute → Verify](reference-architectures/plan-approve-execute-verify.md)

A governed infrastructure-change pattern that separates AI-generated planning from deterministic validation, policy enforcement, human approval, controlled execution, rollback, and verification.

---

## Architecture Approach

My architecture practice emphasizes:

- separating assumptions from facts
- making acceptance criteria explicit
- validating important unknowns before production acceptance
- treating operational fit and supportability as architecture requirements
- preferring appropriate complexity over maximum capability
- using automation to improve repeatability without obscuring the system
- keeping authority outside probabilistic AI systems
- documenting decisions, evidence, limitations, and unresolved questions
- leaving enough context for other engineers to operate, challenge, and improve the architecture

See [Architectural Philosophy](architectural-philosophy.md) and [Architecture Practice & Leadership](portfolio/architecture-practice.md).

---

## Core Domains

- AI Infrastructure & High-Performance Networking
- Enterprise Architecture
- Data Center & Multi-Cloud Networking
- Infrastructure Automation
- Governed Agentic Systems & MCP
- Architecture Validation, Leadership & Enablement

<hr style="margin-top: 1em; margin-bottom: 0.6em;" />

<p style="text-align: center; font-size: 0.65em; color: #999; margin-top: 0.4em; margin-bottom: 0;">
  Robert N. Myhre · Architecture Snapshot · <a href="https://robert-n-myhre.github.io/architecture-portfolio" style="color: #999;">robert-n-myhre.github.io/architecture-portfolio</a>
</p>
