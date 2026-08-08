# Multi-Cloud Architecture: Preserving Patterns Without Forcing Symmetry

**Role:** Cloud Networking Architect / Consultant
**Context:** SaaS / cloud-native enterprise
**Status:** Completed
**Selected Architecture:** Azure hub-and-spoke with centralized Palo Alto inspection
**Delivery Model:** Terraform aligned to established AWS standards

---

## Overview

An organization with an established AWS operating model was expanding into Azure for additional application workloads.

The architecture challenge was not simply to reproduce AWS in another cloud.

The goal was to preserve the principles and operational patterns the team already understood while adapting the implementation to Azure where the platforms differed.

That meant balancing architectural consistency against the risk of forcing artificial symmetry between two cloud environments.

---

## Evaluation Criteria

The design was evaluated against several requirements:

- preserve a familiar hub-and-spoke operating model
- maintain centralized traffic inspection using Palo Alto firewalls
- minimize unnecessary operational and cognitive complexity
- align Terraform structure, naming, and reusable modules across clouds
- adapt cleanly to Azure-specific networking behavior
- keep cost proportional to the size and maturity of the Azure environment
- preserve a practical evolution path if future scale justified a different Azure architecture

---

## Azure Virtual WAN Evaluation

Azure Virtual WAN was considered as an alternative to a custom hub-and-spoke design.

For the size of the Azure environment at the time, the additional cost and architectural abstraction did not provide enough benefit to justify adoption.

Centralized Palo Alto inspection also introduced additional design concessions because the desired firewall model was not a native fit within the Azure Virtual WAN hub architecture.

A custom hub-and-spoke model therefore provided the better balance of cost, operational familiarity, and security integration.

The decision did not eliminate Azure Virtual WAN as a future option. The architecture preserved a reasonable migration path if growth later made its additional capabilities worthwhile.

---

## Preserving Patterns, Not Constructs

Several AWS principles transferred cleanly:

- hub-and-spoke topology
- centralized security inspection
- repeatable infrastructure provisioning
- common naming and repository conventions
- modular Terraform structure

The underlying cloud constructs did not always translate directly.

Azure’s subnet model and several platform services differed from AWS, requiring adaptations in routing, load balancing, addressing, and other cloud-specific constructs.

Those differences were treated as implementation realities rather than reasons to force AWS constructs into Azure.

The objective was architectural familiarity, not technical imitation.

---

## Terraform as an Operating Standard

Terraform consistency was a significant part of the architecture decision.

The organization treated naming conventions, module structure, repository patterns, and deployment workflows as standards that should remain aligned across AWS and Azure wherever practical.

Azure-specific differences still required modifications.

Those exceptions were documented rather than hidden behind an artificial attempt to make the two environments identical.

This allowed engineers to approach the infrastructure through a familiar operating model even when the underlying cloud resources behaved differently.

---

## Outcome

The resulting Azure architecture preserved the organization’s established hub-and-spoke and centralized-inspection principles while adapting the implementation to Azure.

The Terraform structure remained familiar enough to reduce the learning burden for engineers already operating the AWS environment.

At the same time, Azure-specific differences remained visible and documented so that operational familiarity did not come at the expense of accurate troubleshooting or platform understanding.

---

## Architectural Lesson

> **Consistency should reduce cognitive load, not erase meaningful differences.**

Multi-cloud architecture does not require identical implementations.

The more useful goal is to preserve principles, operating patterns, and automation conventions where they provide value while allowing each cloud platform to use constructs appropriate to its own architecture.

In this case, familiar Terraform patterns and a consistent hub-and-spoke security model reduced operational friction.

The architecture still acknowledged that engineers eventually need to understand the real Azure constructs underneath those abstractions, particularly when troubleshooting.

The result was consistency at the level that mattered without forcing symmetry where it did not.
