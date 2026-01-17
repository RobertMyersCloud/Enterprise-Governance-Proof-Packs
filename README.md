<div align="center">

# 🛡️ Enterprise Governance Proof Packs
**Robert Myers, MBA | Senior Identity Governance Leader**

</div>

<div align="center">

![Audit Status](https://img.shields.io/badge/Audit-Ready-success?style=for-the-badge)
![Framework](https://img.shields.io/badge/Framework-NIST_800--53-blue?style=for-the-badge)
![FinOps](https://img.shields.io/badge/FinOps-Practitioner-6c757d?style=for-the-badge)

</div>

---

## Executive Narrative
This repository is a **governance evidence library**: repeatable proof packs that show how enterprise controls are **designed, implemented, verified, and evidenced** across Identity, Cloud Security, and FinOps.

The emphasis is operationally realistic:
- preventative controls where possible (deny/guardrails)
- detective controls where required (logging/alerts)
- measurable accountability (ownership, cadence, evidence)

---

## Repository Structure (Proof Packs)

| Pillar | Folder | What’s inside |
| --- | --- | --- |
| Identity Governance (IGA) | [01_IGA_Framework/](./01_IGA_Framework/) | JML, Access Reviews, Conditional Access, PIM, RBAC |
| Cloud Security Engineering | [02_Cloud_Guardrails/](./02_Cloud_Guardrails/) | Defender for Cloud, Azure Policy Guardrails, Logging Baseline, Key Vault RBAC |
| FinOps Governance | [03_FinOps_Governance/](./03_FinOps_Governance/) | Tagging Standard, Budgets & Alerts, Showback (Forecast vs Actual), Savings Cases |
| Strategy / Risk | [04_Strategy_Risk_Resilience/](./04_Strategy_Risk_Resilience/) | Executive Risk Register, NIST Control Matrix, 6-Month Roadmap |

---

## Proof Pack Index (Quick Links)

### 01 — Identity Governance (IGA)
- [Join / Move / Leave (JML) Lifecycle Workflow](./01_IGA_Framework/JML_Lifecycle_Workflow.md)
- [Access Reviews (Campaign Execution + Evidence)](./01_IGA_Framework/Access_Review_SOP.md)
- [Conditional Access Baseline (MFA + Break-Glass + Exceptions)](./01_IGA_Framework/Conditional_Access_Baseline.md)
- [Privileged Identity Management (PIM) Governance Model](./01_IGA_Framework/PIM_Governance_Model.md)
- [RBAC Least Privilege Map](./01_IGA_Framework/RBAC_Least_Privilege_Map.md)

### 02 — Cloud Security Engineering
- [Defender for Cloud Baseline & Remediation Tracker](./02_Cloud_Guardrails/Defender_Remediation_Plan.md)
- [Azure Policy Guardrails (Preventative Controls + Compliance Evidence)](./02_Cloud_Guardrails/Azure_Policy_Definitions.json)
- [Logging Baseline (Workspace + Retention + Alerts)](./02_Cloud_Guardrails/Logging_&_KQL_Library.md)
- [Key Vault Access Model (RBAC + Secret Access Proof)](./02_Cloud_Guardrails/KeyVault_RBAC_Security.md)

### 03 — FinOps Governance
- [Tag + Allocation Standard (Cost Center + Application + Owner)](./03_FinOps_Governance/Tagging_Allocation_Standard.md)
- [Budgets + Alerts (Per Team)](./03_FinOps_Governance/Budget_Alert_Thresholds.md)
- [Showback Template (Forecast vs Actual)](./03_FinOps_Governance/Monthly_Showback_Template.md)
- [Savings Cases (Rightsizing + Storage Tiering)](./03_FinOps_Governance/Savings_Cases_Rightsizing.md)

### 04 — Strategy / Risk
- [Executive Risk Register](./04_Strategy_Risk_Resilience/Executive_Risk_Register.md)
- [NIST 800-53 Master Control Matrix](./04_Strategy_Risk_Resilience/NIST_800-53_Control_Matrix.md)
- [Identity & Governance Maturity Roadmap (6-Month Vision)](./04_Strategy_Risk_Resilience/Identity_Maturity_Roadmap.md)

---

## Evidence Standards
Each proof pack includes:
- Strategic goal and governance decisions (design intent)
- Operating baseline (assumptions)
- Implementation steps (only what matters)
- Verification (expected vs observed)
- Evidence artifacts indexed under the pack’s `evidence/` folder

See: [EVIDENCE_STANDARDS.md](./EVIDENCE_STANDARDS.md)

---

## Advocacy (footer)
![Advocacy](https://img.shields.io/badge/Advocate-Kidney%20Cancer%20Foundation-orange?style=for-the-badge&logo=heart)

I support the Kidney Cancer Foundation as part of a broader commitment to resilience and mission-first leadership.
