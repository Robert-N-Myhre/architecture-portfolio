# SDA-Based East-West Segmentation Strategy (In Progress)

**Role:** Principal Network Architect  
**Industry:** Healthcare
**Status:** In Progress  
**Key Technologies:** Software-Defined Access (SDA), ISE, SDN, Segmentation Policy, Ansible, Lab Automation, Stakeholder Alignment

---

## Overview

The organization had previously implemented perimeter firewalls to control North-South traffic. I was brought in to lead the next phase—**East-West segmentation** across hospitals, clinics, and office locations. This required not just a technical solution, but also a collaborative framework across multiple teams to identify, design, and validate secure segmentation policies.

---

## Objective

- Define a scalable East-West segmentation model based on device criticality and operational roles  
- Implement policy controls that minimize risk without introducing operational complexity  
- Build and test an SDN-based fabric to support dynamic segmentation  
- Restore confidence in access control technologies after a previous NAC initiative failed to gain adoption

---

## Approach

- Collaborated with architects from security, infrastructure, and clinical teams to define **eight segmentation zones**  
- Created a **VLAN/IP assignment strategy** to support policy mapping at smaller sites  
- Worked closely with an external discovery partner to assist with **device identification and zone mapping** across hundreds of sites  
- Defined the structure and policy model for smaller sites which involved manually re-IP’ing and assigning devices into segmentation zones—executed by engineering teams in coordination with site staff  
- Recognized the need for a **fabric-based solution** at larger sites and initiated a vendor evaluation process  
- Selected **Cisco SDA** for Proof of Concept based on infrastructure readiness and deployment feasibility  
- Authored a **low-level design** and created a set of **eight use cases** representing different topologies for testing in a physical lab  
- While the physical lab was under construction, I used **lab virtualization and automation tools** to simulate the SDA environment  
- Developed **Ansible automation** to dynamically create the underlay necessary for SDA  
- Coordinated training and **internal stakeholder enablement** through recurring working sessions, with an emphasis on rebuilding trust after previous technology friction  
- Aligned external vendor support to assist with advanced SDA testing and integration planning


## Current Status

- Foundational SDA fabric design complete  
- Deploying to smaller locations
- Internal labs and use case simulations actively ongoing  
- Coordinating lab-to-production path and final test plans for segmentation policy rollout

---

## Lessons & Reflections

This engagement is a powerful example of how architecture isn’t just about tools—it's about people, process, and trust. Leading teams through technical and cultural change requires more than a diagram. The foundation we’ve built will enable a secure, scalable, and policy-driven infrastructure to evolve over time.

---

## Tags

`#SDA` `#Segmentation` `#EastWest` `#ISE` `#SDN` `#ZeroTrust` `#Ansible` `#ArchitectureLeadership` `#InProgress`
