# Enterprise Segmentation Architecture: Evidence-Based Platform Evaluation

**Role:** Principal Architect<br>
**Context:** Large regulated enterprise<br>
**Status:** Platform evaluation completed; architecture direction reassessed<br>
**Evaluated Platform:** Cisco Software-Defined Access (SDA)

> This case study intentionally generalizes organization-specific implementation details, internal findings, and current architecture context. Cisco SDA is identified because its evaluation and resulting decision are central to the architecture case study.

---

## Overview

The organization needed a scalable approach to East-West segmentation as part of a broader enterprise security architecture across a large, operationally diverse environment.

Cisco SDA was selected for deeper validation because it appeared capable of addressing the primary segmentation requirements and was sufficiently aligned with the access environment to justify a serious proof of concept.

The evaluation was deliberately treated as conditional. Selection for validation did not imply selection for production.

---

## Evaluation Criteria

The assessment began with criteria tied to the business problem rather than to a vendor feature list:

- effective segmentation at the VRF level
- acceptable usability and operational complexity
- reduction of spanning-tree dependencies at the access edge
- sufficient troubleshooting and operational visibility
- compatibility with established core infrastructure
- supportability within enterprise operational and organizational constraints

The criteria were allowed to evolve as design and testing exposed dependencies that were not fully visible during initial product selection.

---

## Evaluation Process

The evaluation combined cross-domain requirements development, architecture design, lab validation, automation, stakeholder review, and operational-readiness assessment.

Different implementation contexts were considered independently rather than assuming one architecture pattern would fit every environment.

Lab work was used to test architecture behavior before production acceptance, while automation helped make portions of the environment repeatable and separate underlying infrastructure preparation from platform-specific evaluation.

---

## Findings

Two findings materially changed the architecture direction.

### Platform coupling

The proposed architecture introduced tighter operational dependencies across policy, control, and switching components than the organization was prepared to accept.

The components could not be evaluated independently. Their lifecycle, synchronization, availability, troubleshooting, and operational dependencies had to be considered as one architecture.

### Existing infrastructure fit

The proposed SDA design did not integrate with the established core infrastructure in a way that satisfied the project’s migration, operational, and investment constraints.

Addressing that mismatch would have required a broader infrastructure transition than could reasonably be justified for the segmentation problem being solved.

These findings did not mean that Cisco SDA was inherently unsuitable as a platform. They meant that the evaluated architecture did not fit the requirements and constraints of this specific enterprise challenge well enough to justify production adoption.

---

## Decision

Validation changed the original platform direction.

Cisco SDA was no longer recommended as the strategic architecture for this specific business challenge.

The evidence showed that satisfying the functional segmentation requirement was not enough to justify production acceptance.

---

## Architectural Lesson

> **Selection for validation is not selection for production.**

A candidate architecture remains conditional until the important assumptions have been tested.

In this case, the evaluation began by asking whether the platform could provide the required segmentation. Better evidence changed the more important question to:

> **Can this architecture be operated, supported, and trusted within the constraints of this enterprise?**

That change in question changed the decision.

The value of the architecture process was not proving that the initially selected platform could be deployed. It was producing enough evidence to determine whether it should be.
