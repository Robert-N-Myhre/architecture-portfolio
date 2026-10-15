# Repository guidance — Independent Technology Research

This is the source of a public **independent technology research** site built with MkDocs Material and published at https://robert-n-myhre.github.io/architecture-portfolio/.

## Purpose and boundaries

This is not a technical résumé, job-search brochure, or employer project showcase. It publishes explorations initiated by personal curiosity about technologies, systems, and architectural questions. Exclude employer- or client-directed work, professional achievement bullet lists, organizational outcomes, and promotional career framing.

Do not invent an independent origin for projects undertaken for others. Review provenance before including new material. Independently explored enterprise use cases are allowed; organizational delivery is not the inclusion criterion.

A project may be experimental, prototype-driven, architectural, or purely conceptual. Implementation is **not** a publication requirement. Preserve research questions, evolving assumptions, negative results, abandoned avenues, and genuine uncertainties. Distinguish clearly between design intent, hypothesis, observed data, prototype validation, and production validation. Never describe a proposed control as proven or a prototype as a deployment.

Write for technically curious readers who have no previous project context. Prefer clear questions, evidence, limitations, and what changed over claims of impact or seniority. Avoid forcing varied research into a rigid template.

## Navigation and content

- `mkdocs.yml` owns site navigation; pages need appropriate nav entries to appear.
- `docs/projects/` holds investigations.
- `docs/reference-architectures/` holds research-derived and conceptual architecture artifacts; label their maturity.
- `docs/research-methodology.md` describes evidence and publication principles.
- `docs/assets/` contains visual assets and CSS; preserve assets used by active pages.
- `overrides/` contains Material theme overrides.

Maintain existing public investigation URLs unless there is a compelling reason to change them. Do not change deployed content silently if status, evidence, or scope changes.

## Preview and build

```bash
mkdocs serve
mkdocs build --strict
```

The `.github/workflows/gh-pages.yml` workflow deploys on pushes to `main`. Prefer a reviewable PR for broad content changes. Verify internal links and images after restructuring.
