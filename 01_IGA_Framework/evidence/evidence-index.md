# Evidence Index — Identity Governance (IGA)

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)

---

## Evidence Naming Standard
See: [SCREENSHOT_NAMING_STANDARD.md](../../SCREENSHOT_NAMING_STANDARD.md)

---

## Packs

# 01 — IGA Evidence Index

**Pillar:** Identity Governance (IGA)  
**Audience:** Recruiters / Hiring Managers / Auditors  
**Change policy:** IMMUTABLE once associated packs are marked COMPLETE

---

## Evidence Sets

### Conditional Access Baseline (MFA + Break-Glass + Exceptions)
| Evidence ID | Artifact | What it proves |
| --- | --- | --- |
| EV-2026-01-17-001 | [EV-2026-01-17-001_ca_license_gate.png](./EV-2026-01-17-001_ca_license_gate.png) | Conditional Access policy creation is license-gated (no Entra ID Premium) |
| EV-2026-01-17-002 | [EV-2026-01-17-002_security_defaults_enabled.png](./EV-2026-01-17-002_security_defaults_enabled.png) | Security Defaults are enabled (baseline MFA posture) |
| EV-2026-01-17-003 | [EV-2026-01-17-003_auth_methods_policy.png](./EV-2026-01-17-003_auth_methods_policy.png) | Authentication Methods Policy is configured (method governance) |
| EV-2026-01-17-004 | [EV-2026-01-17-004_breakglass_accounts_exist.png](./EV-2026-01-17-004_breakglass_accounts_exist.png) | Two break-glass accounts exist (emergency access path) |
| EV-2026-01-17-005 | [EV-2026-01-17-005_breakglass_global_admin.png](./EV-2026-01-17-005_breakglass_global_admin.png) | Break-glass accounts have privileged role assignment (Global Admin) |
| EV-2026-01-17-006 | [EV-2026-01-17-006_signin_visibility_basic.png](./EV-2026-01-17-006_signin_visibility_basic.png) | Sign-in logs are available and reviewable |
| EV-2026-01-17-007 | [EV-2026-01-17-007_mfa_registration_report.png](./EV-2026-01-17-007_mfa_registration_report.png) | MFA registration reporting is premium-gated (constraint evidence) |
| EV-2026-01-17-008 | [EV-2026-01-17-008_user_authentication_methods.png](./EV-2026-01-17-008_user_authentication_methods.png) | User auth methods exist; TAP present (operational capability) |
| EV-2026-01-17-009 | [EV-2026-01-17-009_signin_event_auth_details_mfa.png](./EV-2026-01-17-009_signin_event_auth_details_mfa.png) | MFA enforcement state is observable in sign-in telemetry (“Previously satisfied”) |

---

## Notes
- Evidence is stored in this folder to ensure stable relative linking from the pack documents.
- All screenshots must follow repo screenshot naming and sanitization standards.

### Access Reviews
Pack: [`../Access_Review_SOP.md`](../Access_Review_SOP.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | Campaign created with scope + owners | `./YYYYMMDD_iga_accessreviews_ev01_campaign_setup.png` |
| EV-02 | Decisions recorded (approve/remove) | `./YYYYMMDD_iga_accessreviews_ev02_decisions.png` |
| EV-03 | Removal executed and verified | `./YYYYMMDD_iga_accessreviews_ev03_access_removed.png` |

### Conditional Access Baseline
Pack: [`../Conditional_Access_Baseline.md`](../Conditional_Access_Baseline.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | CA policies exist and match baseline | `./YYYYMMDD_iga_ca_ev01_policy_list.png` |
| EV-02 | MFA enforced for target users | `./YYYYMMDD_iga_ca_ev02_signin_mfa.png` |
| EV-03 | Legacy auth blocked / logged | `./YYYYMMDD_iga_ca_ev03_legacy_block.png` |

### PIM Governance Model
Pack: [`../PIM_Governance_Model.md`](../PIM_Governance_Model.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | Roles eligible (no standing admin) | `./YYYYMMDD_iga_pim_ev01_role_settings.png` |
| EV-02 | Activation requires MFA/justification | `./YYYYMMDD_iga_pim_ev02_activation.png` |
| EV-03 | Audit logs show activation + expiry | `./YYYYMMDD_iga_pim_ev03_audit_log.png` |

### RBAC Least Privilege Map
Pack: [`../RBAC_Least_Privilege_Map.md`](../RBAC_Least_Privilege_Map.md)

| Evidence ID | What this proves | Artifact |
| --- | --- | --- |
| EV-01 | Group-based role assignment model | `./YYYYMMDD_iga_rbac_ev01_group_model.png` |
| EV-02 | Role assignment at correct scope | `./YYYYMMDD_iga_rbac_ev02_scope_assignment.png` |
| EV-03 | Quarterly review evidence exists | `./YYYYMMDD_iga_rbac_ev03_review_record.png` |

---
