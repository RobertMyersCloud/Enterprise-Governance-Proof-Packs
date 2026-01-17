# Executive Risk Register (Identity, Cloud, FinOps)

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)
![Audience: Executive/Auditors](https://img.shields.io/badge/Audience-Executive%20%2F%20Auditors-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** Once marked **COMPLETE**, this register is **IMMUTABLE**. Updates require formal risk reassessment and linkage to updated proof packs.

---

## Purpose
This Executive Risk Register identifies **material enterprise risks** across Identity, Cloud Security, and FinOps, and maps them directly to **implemented technical controls** contained within this repository.

It serves as:
- A board-level risk communication artifact
- An audit navigation document
- A justification for governance investment and leadership accountability

---

## Risk Scoring Method
| Dimension | Description |
| --- | --- |
| Likelihood | Probability of occurrence |
| Impact | Business, financial, or operational damage |
| Rating | Low / Medium / High |
| Treatment | Mitigate / Accept / Transfer |

---

## Enterprise Risk Register

### R-101 — Identity Takeover (Privileged Account Compromise)
| Attribute | Detail |
| --- | --- |
| Category | Identity Security |
| Likelihood | Medium |
| Impact | High |
| Risk Rating | High |
| Primary Threat | Credential theft, MFA bypass, admin abuse |

**Mitigating Controls**
- Conditional Access Baseline
- PIM Governance Model
- Break-glass governance
- Logging Baseline

**Evidence**
- `01_IGA_Framework/Conditional_Access_Baseline.md`
- `01_IGA_Framework/PIM_Governance_Model.md`
- `02_Cloud_Guardrails/Logging_&_KQL_Library.md`

**Audit Mapping**
- NIST 800-53: IA-2, AC-2, AC-6

---

### R-102 — Privilege Creep (Mover Drift)
| Attribute | Detail |
| --- | --- |
| Category | Identity Governance |
| Likelihood | High |
| Impact | Medium |
| Risk Rating | High |
| Primary Threat | Excess access retained after role change |

**Mitigating Controls**
- JML Lifecycle Workflow
- Access Review Campaigns
- RBAC Least Privilege Model

**Evidence**
- `01_IGA_Framework/JML_Lifecycle_Workflow.md`
- `01_IGA_Framework/Access_Review_SOP.md`
- `01_IGA_Framework/RBAC_Least_Privilege_Map.md`

**Audit Mapping**
- NIST 800-53: AC-2, AC-5

---

### R-201 — Cloud Misconfiguration (Preventable Exposure)
| Attribute | Detail |
| --- | --- |
| Category | Cloud Security |
| Likelihood | Medium |
| Impact | High |
| Risk Rating | High |
| Primary Threat | Unsafe resource deployments |

**Mitigating Controls**
- Azure Policy Guardrails
- Defender for Cloud Baseline
- Logging Baseline

**Evidence**
- `02_Cloud_Guardrails/Azure_Policy_Definitions.json`
- `02_Cloud_Guardrails/Defender_Remediation_Plan.md`

**Audit Mapping**
- NIST 800-53: CM-6, SI-2, SI-4

---

### R-202 — Secret Exposure (Credential Leakage)
| Attribute | Detail |
| --- | --- |
| Category | Secrets Management |
| Likelihood | Medium |
| Impact | High |
| Risk Rating | High |
| Primary Threat | Hardcoded secrets, shared access |

**Mitigating Controls**
- Key Vault RBAC Access Model
- Logging Baseline
- Break-glass monitoring

**Evidence**
- `02_Cloud_Guardrails/KeyVault_RBAC_Security.md`
- `02_Cloud_Guardrails/Logging_&_KQL_Library.md`

**Audit Mapping**
- NIST 800-53: IA-5, SC-28

---

### R-301 — Unattributed Cloud Spend
| Attribute | Detail |
| --- | --- |
| Category | FinOps |
| Likelihood | High |
| Impact | Medium |
| Risk Rating | High |
| Primary Threat | Missing ownership, uncontrolled spend |

**Mitigating Controls**
- Tagging & Allocation Standard
- Showback Reporting
- Budget Alerts

**Evidence**
- `03_FinOps_Governance/Tagging_Allocation_Standard.md`
- `03_FinOps_Governance/Monthly_Showback_Template.md`
- `03_FinOps_Governance/Budget_Alert_Thresholds.md`

**Audit Mapping**
- FinOps Framework (Allocation, Accountability)

---

### R-302 — Cost Overrun (Budget Breach)
| Attribute | Detail |
| --- | --- |
| Category | Financial Governance |
| Likelihood | Medium |
| Impact | High |
| Risk Rating | High |
| Primary Threat | Unmonitored consumption growth |

**Mitigating Controls**
- Budgets + Alerts
- Showback + Forecast
- Savings Case Governance

**Evidence**
- `03_FinOps_Governance/Budget_Alert_Thresholds.md`
- `03_FinOps_Governance/Savings_Cases_Rightsizing.md`

---

## Executive Summary
This register demonstrates that **enterprise risks are not theoretical**—they are actively governed through documented controls, monitored through evidence, and reviewed on a defined cadence.

Governance is not implemented for compliance alone; it is used to:
- Reduce operational risk
- Protect revenue and reputation
- Enable scalable cloud growth

---

## Navigation
- Repo README: `../README.md`
- Strategy README: `./README.md`
