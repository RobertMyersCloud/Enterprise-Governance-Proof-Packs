# NIST 800-53 Master Control Matrix

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)
![Audience: Executive/Auditors](https://img.shields.io/badge/Audience-Executive%20%2F%20Auditors-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** Once marked **COMPLETE**, this matrix is **IMMUTABLE**. Control mappings may only change if the underlying control implementation changes.

---

## Purpose
This Master Control Matrix maps **implemented technical controls** in this repository to **NIST SP 800-53 security control families**.

It serves as:
- An audit navigation guide
- Proof of control coverage
- A bridge between governance language and engineering execution

---

## How to Use This Matrix
- **Auditors:** Use the Control ID column to locate evidence quickly.
- **Leadership:** Understand which enterprise risks are mitigated.
- **Engineers:** See how technical implementations satisfy formal controls.

Each control maps to **one or more Proof Packs** in this repository.

---

## Identity & Access Management Controls

| NIST Control | Control Description | Implementation | Evidence |
| --- | --- | --- | --- |
| AC-2 | Account Management | JML Workflow + Access Reviews | `01_IGA_Framework/JML_Lifecycle_Workflow.md` |
| AC-5 | Separation of Duties | RBAC Model + PIM | `01_IGA_Framework/RBAC_Least_Privilege_Map.md` |
| AC-6 | Least Privilege | RBAC + PIM Governance | `01_IGA_Framework/PIM_Governance_Model.md` |
| IA-2 | Identification & Authentication | Conditional Access Baseline (MFA) | `01_IGA_Framework/Conditional_Access_Baseline.md` |
| IA-5 | Authenticator Management | Key Vault RBAC + MFA | `02_Cloud_Guardrails/KeyVault_RBAC_Security.md` |

---

## Privileged Access & Governance Controls

| NIST Control | Control Description | Implementation | Evidence |
| --- | --- | --- | --- |
| AC-2(5) | Privileged Account Monitoring | PIM Activation Logs | `01_IGA_Framework/PIM_Governance_Model.md` |
| AC-6(2) | Privilege Elevation Control | JIT Role Activation | `01_IGA_Framework/PIM_Governance_Model.md` |
| AU-2 | Auditable Events | Logging Baseline | `02_Cloud_Guardrails/Logging_&_KQL_Library.md` |
| AU-12 | Audit Log Generation | Entra + Azure Activity Logs | `02_Cloud_Guardrails/Logging_&_KQL_Library.md` |

---

## Configuration & Change Management Controls

| NIST Control | Control Description | Implementation | Evidence |
| --- | --- | --- | --- |
| CM-2 | Baseline Configuration | Azure Policy Guardrails | `02_Cloud_Guardrails/Azure_Policy_Definitions.json` |
| CM-6 | Configuration Settings | Policy Deny Enforcement | `02_Cloud_Guardrails/Azure_Policy_Definitions.json` |
| SI-2 | Flaw Remediation | Defender Remediation Tracker | `02_Cloud_Guardrails/Defender_Remediation_Plan.md` |
| SI-4 | System Monitoring | Defender + Log Alerts | `02_Cloud_Guardrails/Defender_Remediation_Plan.md` |

---

## Data Protection & Secrets Management

| NIST Control | Control Description | Implementation | Evidence |
| --- | --- | --- | --- |
| SC-28 | Protection of Information at Rest | Key Vault RBAC + Logging | `02_Cloud_Guardrails/KeyVault_RBAC_Security.md` |
| IA-7 | Cryptographic Key Management | Key Vault Governance | `02_Cloud_Guardrails/KeyVault_RBAC_Security.md` |

---

## Financial Governance (FinOps Alignment)

| NIST / Governance Area | Control Objective | Implementation | Evidence |
| --- | --- | --- | --- |
| PL-2 (Governance) | Financial Accountability | Tagging & Allocation Standard | `03_FinOps_Governance/Tagging_Allocation_Standard.md` |
| CA-7 | Continuous Monitoring | Budget Alerts + Showback | `03_FinOps_Governance/Budget_Alert_Thresholds.md` |
| RA-3 | Risk Assessment | Savings Case Analysis | `03_FinOps_Governance/Savings_Cases_Rightsizing.md` |

---

## Control Coverage Summary
- **Identity & Access:** Covered via IGA + PIM + CA
- **Cloud Security:** Covered via Policy + Defender + Logging
- **Secrets:** Covered via Key Vault RBAC
- **Financial Governance:** Covered via FinOps Proof Packs

This matrix demonstrates **end-to-end governance coverage**, not isolated controls.

---

## Navigation
- Repo README: `../README.md`
- Strategy README: `./README.md`
- Executive Risk Register: `./Executive_Risk_Register.md`
