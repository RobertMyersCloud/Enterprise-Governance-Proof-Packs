# Evidence Index — Cloud Security Engineering

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)

---

## Evidence Naming Standard
See: [SCREENSHOT_NAMING_STANDARD.md](../../SCREENSHOT_NAMING_STANDARD.md)

---

## Packs

### Defender for Cloud Baseline & Remediation
Pack: [`../Defender_Remediation_Plan.md`](../Defender_Remediation_Plan.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | Baseline posture captured | `./YYYYMMDD_cloud_defender_ev01_secure_score.png` |
| EV-02 | Recommendation triage + ownership | `./YYYYMMDD_cloud_defender_ev02_recommendations.png` |
| EV-03 | Remediation completed + validated | `./YYYYMMDD_cloud_defender_ev03_post_fix.png` |

### Azure Policy Guardrails
Pack: [`../Azure_Policy_Definitions.json`](../Azure_Policy_Definitions.json)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | Policy assignments exist at scope | `./YYYYMMDD_cloud_policy_ev01_assignment.png` |
| EV-02 | Deny event logged on noncompliance | `./YYYYMMDD_cloud_policy_ev02_deny_event.png` |
| EV-03 | Compliance report export captured | `./YYYYMMDD_cloud_policy_ev03_compliance.png` |

### Logging Baseline
Pack: [`../Logging_&_KQL_Library.md`](../Logging_&_KQL_Library.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | LAW created + diagnostics enabled | `./YYYYMMDD_cloud_logging_ev01_law_settings.png` |
| EV-02 | Tables populated (ingestion proof) | `./YYYYMMDD_cloud_logging_ev02_tables.png` |
| EV-03 | Alert rule configured + fires | `./YYYYMMDD_cloud_logging_ev03_alert.png` |

### Key Vault Access Model
Pack: [`../KeyVault_RBAC_Security.md`](../KeyVault_RBAC_Security.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | RBAC model configured for vault | `./YYYYMMDD_cloud_keyvault_ev01_rbac.png` |
| EV-02 | Secret access logged | `./YYYYMMDD_cloud_keyvault_ev02_access_log.png` |
| EV-03 | Review/approval evidence exists | `./YYYYMMDD_cloud_keyvault_ev03_review.png` |

---
