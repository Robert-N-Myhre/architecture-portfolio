<div class="snapshot-shell">

<section class="snapshot-hero">
  <p class="snapshot-kicker">Architecture Portfolio</p>
  <h1 class="snapshot-name">Robert N. Myhre</h1>
  <p class="snapshot-role">Principal Infrastructure Architect | Cross-Domain Architecture & Technology Strategy</p>
  <p class="snapshot-lede">
    I work where enterprise infrastructure, cloud, security, platform engineering, automation, and emerging technology intersect—connecting constraints across domains and turning them into architecture that organizations can build, operate, govern, and sustain.
  </p>
  <p class="snapshot-tagline">Architecting solutions that others can build on.</p>
  <div class="snapshot-actions">
    <a href="#enterprise-architecture-decisions">Explore Selected Work</a>
    <a href="#architecture-approach">How I Architect</a>
    <a href="https://robert-n-myhre.github.io/architecture-portfolio">Full Portfolio</a>
  </div>
  <div class="snapshot-meta">
    <span>CCIE #9837 (Active)</span>
    <span><a href="mailto:ccie9837@gmail.com">ccie9837@gmail.com</a></span>
    <span><a href="https://www.linkedin.com/in/robert-n-myhre">LinkedIn</a> · <a href="https://github.com/Robert-N-Myhre">GitHub</a></span>
  </div>
</section>

<section class="snapshot-section">
  <div class="snapshot-section-head">
    <h2 id="enterprise-architecture-decisions">Enterprise Architecture Decisions</h2>
    <p>Selected case studies centered on architectural tradeoffs, evidence, constraints, and decisions made under real enterprise conditions.</p>
  </div>

  <div class="snapshot-grid">
    <a class="snapshot-card" href="projects/dc-aci-project.md">
      <p class="eyebrow">Architecture Decision</p>
      <h3>Dual Data Center Architecture</h3>
      <p>Choosing the right fabric model by balancing policy consistency, resiliency, migration, and operational complexity.</p>
      <span class="card-link">View case study →</span>
    </a>

    <a class="snapshot-card" href="projects/multicloud-network-architecture.md">
      <p class="eyebrow">Architecture Decision</p>
      <h3>Multi-Cloud Network-as-a-Service</h3>
      <p>Replacing repeated circuit procurement with a reusable connectivity model while managing resiliency and provider dependency.</p>
      <span class="card-link">View case study →</span>
    </a>

    <a class="snapshot-card" href="projects/multicloud-terraform.md">
      <p class="eyebrow">Architecture Decision</p>
      <h3>Preserving Patterns Without Forcing Symmetry</h3>
      <p>Extending an AWS operating model into Azure while preserving intent without pretending the two platforms are identical.</p>
      <span class="card-link">View case study →</span>
    </a>

    <a class="snapshot-card" href="projects/sda-segmentation.md">
      <p class="eyebrow">Architecture Decision</p>
      <h3>Enterprise Segmentation Evaluation</h3>
      <p>Using explicit acceptance criteria, lab validation, automation, and stakeholder review to let evidence change the recommendation.</p>
      <span class="card-link">View case study →</span>
    </a>
  </div>
</section>

<section class="snapshot-section">
  <div class="snapshot-section-head">
    <h2>Emerging Technology & AI Infrastructure</h2>
    <p>Hands-on architecture research used to test assumptions, expose constraints, and determine where emerging designs are supportable.</p>
  </div>

  <div class="snapshot-grid">
    <a class="snapshot-card" href="projects/intelligence-placement-under-constraint.md">
      <p class="eyebrow">Systems Architecture</p>
      <h3>Intelligence Placement Under Constraint</h3>
      <p>Reasoning about where enterprise AI should execute and how latency, locality, governance, cost, failure, and trust shape placement.</p>
      <span class="card-link">Explore framework →</span>
    </a>

    <a class="snapshot-card" href="projects/mcp-platform-case-study.md">
      <p class="eyebrow">Architecture Validation</p>
      <h3>MCP Platform Case Study</h3>
      <p>A working centralized platform that was deliberately stopped when evidence showed the abstraction was not reducing integration cost.</p>
      <span class="card-link">View case study →</span>
    </a>

    <a class="snapshot-card" href="projects/moe-routing-observability.md">
      <p class="eyebrow">Infrastructure Research</p>
      <h3>MoE Routing Observability</h3>
      <p>Multi-GPU investigation of routing behavior, topology, communication, placement, and observability beyond aggregate throughput.</p>
      <span class="card-link">View research →</span>
    </a>

    <a class="snapshot-card" href="projects/prompt-guardrail-single-gpu.md">
      <p class="eyebrow">Governed AI</p>
      <h3>Prompt Security Guardrails</h3>
      <p>Testing workload co-residency and demonstrating why deterministic controls must keep authority outside probabilistic models.</p>
      <span class="card-link">View research →</span>
    </a>
  </div>
</section>

<section class="snapshot-section">
  <div class="snapshot-section-head">
    <h2>Reference Architectures</h2>
    <p>Vendor-neutral patterns for governed automation, explicit authority boundaries, deterministic controls, and auditability.</p>
  </div>

  <div class="snapshot-grid">
    <a class="snapshot-card" href="reference-architectures/monitor-classify-escalate.md">
      <p class="eyebrow">Reference Architecture</p>
      <h3>Monitor → Classify → Escalate</h3>
      <p>AI-assisted event triage with structured outputs, deterministic confidence scoring, enrichment, escalation, and auditability.</p>
      <span class="card-link">View architecture →</span>
    </a>

    <a class="snapshot-card" href="reference-architectures/plan-approve-execute-verify.md">
      <p class="eyebrow">Reference Architecture</p>
      <h3>Plan → Approve → Execute → Verify</h3>
      <p>Governed infrastructure mutation separating probabilistic planning from deterministic validation, approval, execution, and verification.</p>
      <span class="card-link">View architecture →</span>
    </a>
  </div>
</section>

<section class="snapshot-section" id="architecture-approach">
  <div class="snapshot-wide-card">
    <h3>Architecture Approach</h3>
    <p>I tend to start with questions rather than products: What problem are we actually solving? Which assumptions are being treated as facts? Where does complexity create operational risk? What should be standardized, and where should flexibility remain?</p>
    <p>I use design, implementation, lab validation, measurement, and documented decisions to reduce uncertainty. The goal is not maximum capability; it is architecture that is understandable, supportable, explicit about its constraints, and able to be handed off without becoming a dependency on the architect.</p>
    <p><a href="architectural-philosophy.md">Architectural Philosophy</a> · <a href="portfolio/architecture-practice.md">Architecture Practice & Leadership</a></p>

    <div class="snapshot-domain-row">
      <span class="snapshot-domain">Cross-Domain Enterprise Architecture</span>
      <span class="snapshot-domain">Enterprise Infrastructure & Networking</span>
      <span class="snapshot-domain">Cloud & Platform Engineering</span>
      <span class="snapshot-domain">Security & Segmentation</span>
      <span class="snapshot-domain">Infrastructure Automation & IaC</span>
      <span class="snapshot-domain">AI Infrastructure & Emerging Technology</span>
      <span class="snapshot-domain">Architecture Governance & Enablement</span>
    </div>
  </div>
</section>

<div class="snapshot-footer">
  Robert N. Myhre · Architecture Snapshot · <a href="https://robert-n-myhre.github.io/architecture-portfolio">Full Architecture Portfolio</a>
</div>

</div>
