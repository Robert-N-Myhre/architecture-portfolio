<div style="display: flex; justify-content: space-between; align-items: flex-start;">

<div style="line-height: 1.3; margin-top: 0;">
  <h1 style="margin-bottom: 0.2em;">Robert N. Myhre, CCIE #9837 (Active)</h1>
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

Hands-on projects and case studies used to test architectural assumptions, measure behavior, and identify where designs succeed or fail.

- **[MCP Platform Case Study](projects/mcp-platform-case-study.md)**
  Built and validated a centralized MCP platform, then rejected the reusable-platform hypothesis when implementation evidence showed the abstraction was not reducing integration cost.

- **[MoE Routing Observability](projects/moe-routing-observability.md)**
  Multi-GPU investigation of mixture-of-experts routing, topology, communication behavior, and observability.

- **[Prompt Guardrail / Single-GPU Co-residency](projects/prompt-guardrail-single-gpu.md)**
  Experimental evaluation of guardrail and workload co-residency constraints on a single GPU.

### Enterprise Infrastructure Architecture

Selected architecture work spanning data center, cloud, segmentation, connectivity, and automation.

- [Dual Data Center Architecture with Cisco ACI](projects/dc-aci-project.md)
- [Multi-Cloud Connectivity via Megaport MCRs](projects/multicloud-network-architecture.md)
- [Azure Multi-Cloud Expansion with Terraform](projects/multicloud-terraform.md)
- [SDA-Based East-West Segmentation Strategy](projects/sda-segmentation.md)

---

## Reference Architectures

Reusable architecture patterns focused on governed automation, explicit authority boundaries, deterministic controls, and auditability.

- [Monitor → Classify → Escalate](reference-architectures/monitor-classify-escalate.md)
- [Plan → Approve → Execute → Verify](reference-architectures/plan-approve-execute-verify.md)

---

## Architecture Practice

My architecture work is grounded in a simple principle: emerging technology becomes useful only when its assumptions, constraints, operational boundaries, and failure modes are understood.

I use design, implementation, lab validation, measurement, and documented decisions to determine what is supportable, what needs to change, and sometimes what should not be built.

- [Architectural Philosophy](architectural-philosophy.md)
- [About Me](about.md)
