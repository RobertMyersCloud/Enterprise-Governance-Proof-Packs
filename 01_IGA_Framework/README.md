# 🏛️ Identity Governance Framework (IGA)

![Status: ACTIVE](https://img.shields.io/badge/Status-ACTIVE-0d6efd?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)
![Audience: Recruiters/Auditors](https://img.shields.io/badge/Audience-Recruiters%20%2F%20Auditors-212529?style=for-the-badge)

---

## Purpose
This pillar documents **enterprise identity governance controls** that manage the full identity lifecycle—from onboarding to privilege elevation to separation—using **defensible design, controlled execution, and auditable evidence**.

The focus is **governance**, not tooling:
- controls are intentional
- access is reviewable
- exceptions are traceable
- evidence supports audit review

---

## Scope
This framework governs **who gets access, how access is granted, how privilege is controlled, and how access is reviewed over time**.

**In scope**
- Join / Move / Leave (JML) lifecycle governance
- Authentication enforcement baseline (MFA + break-glass)
- Privileged Identity Management (PIM)
- Role-Based Access Control (RBAC)
- Periodic access reviews
- Evidence capture and retention

**Out of scope (by design)**
- Endpoint device management
- Application-specific entitlement engines
- Custom IAM product implementation
- Advanced Conditional Access features requiring premium licensing

---

## Governance Principles
- **Least Privilege:** Access is granted only as required by job function
- **Separation of Duties:** Privileged paths are isolated and elevated explicitly
- **Time-Bound Access:** Standing privilege is avoided
- **Business Ownership:** Access decisions are owned outside of IT
- **Audit Defensibility:** Design intent and effectiveness are provable

---

## Proof Packs (IGA)

| Pack | Focus | Status |
| --- | --- | --- |
| **JML Lifecycle Workflow** | Identity onboarding, role change, and separation governance | ACTIVE |
| **Conditional Access Baseline** | MFA enforcement, break-glass governance (Security Defaults) | **COMPLETE / IMMUTABLE** |
| **PIM Governance Model** | Just-In-Time admin access + auditability | ACTIVE |
| **RBAC Least Privilege Map** | Department roles → permission boundaries | ACTIVE |
| **Access Reviews** | Periodic certification + evidence | ACTIVE |

---

## Pack Index (Clickable)

### Identity Lifecycle
- [`JML_Lifecycle_Workflow.md`](./JML_Lifecycle_Workflow.md)

### Authentication & Privilege
- [`Conditional_Access_Baseline.md`](./Conditional_Access_Baseline.md)
- [`PIM_Governance_Model.md`](./PIM_Governance_Model.md)

### Authorization & Review
- [`RBAC_Least_Privilege_Map.md`](./RBAC_Least_Privilege_Map.md)
- [`Access_Review_SOP.md`](./Access_Review_SOP.md)

---

## Evidence Model
Each proof pack includes:
- Strategic goal and governance decisions (test of design)
- Operating baseline (assumptions)
- Implementation steps (only what matters)
- Verification (expected vs observed)
- Linked evidence artifacts

All evidence is indexed here:
- [`./evidence/evidence-index.md`](./evidence/evidence-index.md)

Evidence artifacts are immutable once referenced by a COMPLETE pack.

---

## Exception Handling
Any deviation from an IMMUTABLE baseline requires:
- documented justification
- explicit scope
- expiration date
- entry into the shared register

See:
- [`../EXCEPTION_REGISTER.md`](../EXCEPTION_REGISTER.md)

---

## Control Mapping
Primary framework alignment:
- **NIST 800-53:** IA-2, AC-2, AC-6, AU-2, AU-12
- **Audit lens:** Test of Design + Test of Effectiveness

---

## Navigation
- Repo Root: [`../README.md`](../README.md)
- Evidence Index: [`./evidence/evidence-index.md`](./evidence/evidence-index.md)
- Exception Register: [`../EXCEPTION_REGISTER.md`](../EXCEPTION_REGISTER.md)

