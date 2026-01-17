# Identity & Governance Maturity Roadmap (6-Month Vision)

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)
![Audience: Executive/Leadership](https://img.shields.io/badge/Audience-Executive%20%2F%20Leadership-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** This roadmap represents an approved strategic direction. Deviations require reassessment of risk, scope, and sequencing.

---

## Purpose
This roadmap defines a **realistic, defensible 6-month progression** from baseline identity hygiene to mature, audit-ready governance.

It balances:
- Risk reduction
- Operational capacity
- Audit readiness
- Business enablement

---

## Maturity Principles
- Identity controls are built **before** scale.
- Privilege is treated as a risk multiplier.
- Financial governance follows technical visibility.
- Each phase produces **auditable artifacts**, not just configuration.

---

## Month 0 — Baseline State (Entry Conditions)
**Assumed starting posture**
- Entra ID tenant exists
- MFA partially enforced
- Limited logging visibility
- Ad-hoc access provisioning
- No standardized cost allocation

This is a common enterprise starting point.

---

## Phase 1 (Months 1–2): Identity Foundation & Access Control

### Objectives
- Eliminate high-risk identity attack paths
- Establish least privilege as default
- Create audit-visible access lifecycle

### Key Deliverables
- Conditional Access Baseline (MFA + legacy auth block)
- Break-glass governance established
- JML Lifecycle Workflow implemented
- RBAC Least Privilege Model documented
- Centralized logging baseline enabled

### Risks Reduced
- Credential stuffing
- Privileged account compromise
- Orphaned accounts

### Evidence Produced
- CA policy definitions
- JML workflow documentation
- RBAC mapping
- Log ingestion proof

---

## Phase 2 (Months 3–4): Privileged Governance & Cloud Guardrails

### Objectives
- Remove standing administrative access
- Prevent unsafe cloud configurations
- Improve detection and response readiness

### Key Deliverables
- PIM Governance Model (JIT + approvals)
- Access Review campaigns executed
- Azure Policy preventative guardrails
- Defender for Cloud baseline with remediation tracking
- Key Vault RBAC access model

### Risks Reduced
- Privilege creep
- Misconfiguration exposure
- Secret leakage

### Evidence Produced
- PIM activation logs
- Access review records
- Policy compliance exports
- Remediation tracker

---

## Phase 3 (Months 5–6): Financial Governance & Executive Alignment

### Objectives
- Tie cloud spend to ownership
- Detect and prevent budget overruns
- Demonstrate measurable value realization

### Key Deliverables
- Tagging & Allocation Standard enforced
- Budgets + Alerts per team
- Monthly Showback (Forecast vs Actual)
- Savings cases (rightsizing + storage tiering)
- Executive Risk Register finalized

### Risks Reduced
- Unattributed spend
- Budget surprises
- Unjustified cloud growth

### Evidence Produced
- Tag compliance reports
- Budget alert history
- Showback reports
- Savings validation

---

## Maturity Outcome (End State)
By month 6, the organization achieves:
- **Zero standing admin access**
- **Preventative cloud guardrails**
- **Auditable identity lifecycle**
- **Executive-level cost visibility**
- **Mapped controls to NIST 800-53**

This represents a **governance-ready cloud posture**, not a theoretical framework.

---

## Success Metrics
| Area | Metric |
| --- | --- |
| Identity | % users protected by MFA |
| Privilege | % admin roles eligible-only |
| Governance | Access review completion rate |
| Security | Reduction in high-risk findings |
| FinOps | % spend attributed to owner |

---

## Navigation
- Repo README: `../README.md`
- Strategy README: `./README.md`
- Executive Risk Register: `./Executive_Risk_Register.md`
- NIST Control Matrix: `./NIST_800-53_Control_Matrix.md`
