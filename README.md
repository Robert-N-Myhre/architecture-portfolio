# Architecture Portfolio

This repository contains the source for my public architecture portfolio:

**https://robert-n-myhre.github.io/architecture-portfolio/**

I am a principal-level infrastructure architect and dual CCIE with more than 25 years in enterprise infrastructure and more than 15 years in architecture roles.

My foundation is enterprise networking, data center, and cloud architecture. My current work increasingly intersects with AI infrastructure, infrastructure automation, and governed agentic systems.

## What the Portfolio Contains

### AI Infrastructure & Agentic Systems

Hands-on research and architecture case studies covering areas such as:

- multi-GPU infrastructure and observability
- Mixture-of-Experts behavior
- GPU topology and resource constraints
- Model Context Protocol (MCP)
- governed agentic infrastructure
- deterministic controls around probabilistic AI systems

### Enterprise Architecture Decisions

Case studies focused on architectural reasoning rather than product implementation, including:

- data center fabric selection
- multi-cloud connectivity models
- cross-cloud operating-pattern alignment
- evidence-based platform evaluation

### Reference Architectures

Vendor-neutral patterns for governed AI-assisted infrastructure operations, including:

- Monitor → Classify → Escalate
- Plan → Approve → Execute → Verify

### Architecture Practice

Material covering architectural decision-making, validation, automation, technical leadership, mentoring, and enablement.

## How I Approach Architecture

My architecture work is evidence-driven.

I separate assumptions from facts, identify the constraints that matter, validate important unknowns, and use the resulting evidence to determine what should be built, what should change, and sometimes what should be stopped.

The portfolio is intended to show not only **what** I have architected, but **how architectural decisions were reached**.

## Repository Structure

```text
docs/
├── projects/                 # Architecture case studies and research
├── reference-architectures/  # Reusable architecture patterns
├── portfolio/                # Architecture practice + legacy landing pages
├── assets/                   # Images, PDFs, and styles
├── index.md                  # Portfolio home page
├── about.md                  # About / professional background
├── architectural-philosophy.md
├── snapshot.md               # Direct LinkedIn architecture snapshot
└── current-focus.md          # Legacy landing page
```

The site is built with **MkDocs Material** and deployed automatically through **GitHub Actions**.
