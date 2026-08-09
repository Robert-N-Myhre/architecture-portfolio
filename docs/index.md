<div style="display: flex; justify-content: space-between; align-items: flex-start;">

<div style="line-height: 1.3; margin-top: 0;">
<div style="font-size: 2em; font-weight: 700; margin-bottom: 0.2em;">
  Robert N. Myhre, CCIE #9837 (Active)
</div>
  <p style="margin: 0;"><strong>Principal Architect | AI Infrastructure, Networking & Automation</strong></p>
  <p style="margin: 0;">✉️ ccie9837@gmail.com</p>
  <p style="margin: 0;">🔗 <a href="https://www.linkedin.com/in/robert-n-myhre">LinkedIn</a></p>
</div>

<div>
  <img src="assets/images/ccie_20years_med.jpg" alt="CCIE Logo" style="width: 150px; margin-left: 20px;" />
</div>

</div>

---

# Architecture Portfolio

I’m a principal-level infrastructure architect and dual CCIE with more than 25 years in enterprise infrastructure and more than 15 years in architecture roles.

My foundation is deep enterprise networking, data center, and cloud architecture. My current architecture work increasingly intersects with AI infrastructure, while my independent research goes deeper into the systems required to operate AI reliably: multi-GPU infrastructure, high-performance networking, observability, governed agentic systems, MCP, infrastructure automation, and enterprise Kubernetes patterns.

This portfolio captures both sides of that work: established enterprise architecture and hands-on investigation of emerging infrastructure systems.

---

## Selected Work

### AI Infrastructure & Agentic Systems

Architecture frameworks, hands-on research, and case studies used to test assumptions, measure behavior, and reason about where AI infrastructure designs succeed, fail, or encounter meaningful constraints.

- **[Intelligence Placement Under Constraint](projects/intelligence-placement-under-constraint.md)**
  A systems-architecture framework for reasoning about where enterprise AI capabilities should execute, how context and decisions flow across layers, and how latency, locality, governance, cost, failure, and trust shape placement.

- **[MCP Platform Case Study](projects/mcp-platform-case-study.md)**
  Built and validated a centralized MCP platform, then rejected the reusable-platform hypothesis when implementation evidence showed the abstraction was not reducing integration cost.

- **[MoE Routing Observability](projects/moe-routing-observability.md)**
  Multi-GPU investigation of mixture-of-experts routing, topology, communication behavior, and observability.

- **[Prompt Security Guardrails](projects/prompt-guardrail-single-gpu.md)**
  Experimental evaluation of guardrail and workload co-residency constraints on a single GPU.

### Enterprise Architecture Decisions

Selected case studies focused on architectural tradeoffs, validation, and decisions made under real enterprise constraints.

- [Dual Data Center Architecture: Choosing the Right Fabric Model](projects/dc-aci-project.md)
- [Multi-Cloud Connectivity: Choosing a Network-as-a-Service Model](projects/multicloud-network-architecture.md)
- [Multi-Cloud Architecture: Preserving Patterns Without Forcing Symmetry](projects/multicloud-terraform.md)
- [Enterprise Segmentation Architecture: Evidence-Based Platform Evaluation](projects/sda-segmentation.md)

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