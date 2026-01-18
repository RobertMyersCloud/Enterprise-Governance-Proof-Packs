# Evidence Index — Identity Governance (IGA)

![Status: COMPLETE](https://img.shields.io/badge/Status-COMPLETE-198754?style=for-the-badge)
![Change Policy: IMMUTABLE](https://img.shields.io/badge/Change%20Policy-IMMUTABLE-212529?style=for-the-badge)

---

## Evidence Naming Standard
All evidence artifacts follow the repository standard:

- Prefix: `EV-YYYY-MM-DD-###`
- Immutable once referenced by a COMPLETE pack
- Screenshots are read-only proof artifacts

See: `SCREENSHOT_NAMING_STANDARD.md`

---

## Packs

### 01 — Identity Governance (IGA)
**Audience:** Recruiters / Hiring Managers / Auditors  
**Change Policy:** IMMUTABLE once associated packs are COMPLETE

---

## Evidence Sets

### Conditional Access Baseline (MFA + Break-Glass + Exceptions)

| Evidence ID | Artifact | What it proves |
| --- | --- | --- |
| EV-2026-01-17-001 | `EV-2026-01-17-001_ca_license_gate.png` | Conditional Access policy creation is license-gated (no Entra ID Premium) |
| EV-2026-01-17-002 | `EV-2026-01-17-002_security_defaults_enabled.png` | Security Defaults are enabled (baseline MFA posture) |
| EV-2026-01-17-003 | `EV-2026-01-17-003_auth_methods_policy.png` | Authentication Methods Policy is configured (method governance) |
| EV-2026-01-17-004 | `EV-2026-01-17-004_breakglass_accounts_exist.png` | Two break-glass accounts exist (emergency access path) |
| EV-2026-01-17-005 | `EV-2026-01-17-005_breakglass_global_admin.png` | Break-glass accounts have privileged role assignment (Global Admin) |
| EV-2026-01-17-006 | `EV-2026-01-17-006_signin_visibility_basic.png` | Sign-in logs are available and reviewable |
| EV-2026-01-17-007 | `EV-2026-01-17-007_mfa_registration_report.png` | MFA registration reporting is premium-gated (documented constraint) |
| EV-2026-01-17-008 | `EV-2026-01-17-008_user_authentication_methods.png` | User authentication methods exist; TAP present (operational capability) |
| EV-2026-01-17-009 | `EV-2026-01-17-009_signin_event_auth_details_mfa.png` | MFA enforcement state observable in sign-in telemetry |

---

## Notes
- This evidence set intentionally documents **both enforcement and constraints**.
- No Conditional Access policies are claimed or implied.
- Enforcement is validated using **Security Defaults + Authentication Methods Policy + sign-in telemetry**.
- Evidence artifacts are immutable and tied to a COMPLETE governance baseline.

---

## Navigation
- Pack: `../Conditional_Access_Baseline.md`
- Pillar README: `../README.md`
- Exception Register: `../../EXCEPTION_REGISTER.md`


---
