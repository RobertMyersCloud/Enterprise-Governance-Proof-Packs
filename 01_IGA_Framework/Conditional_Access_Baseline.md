# ⭐ Conditional Access Baseline (MFA + Break-Glass + Exceptions)
> **Status:** DRAFT • **Audience:** Recruiters/Hiring Managers/Auditors • **Scope:** Entra ID (Azure-first) • **Change policy:** IMMUTABLE once COMPLETE

---

## Goal
Establish a defensible Conditional Access (CA) baseline that enforces MFA for interactive users, protects privileged access paths, and defines controlled exceptions (including break-glass accounts) without weakening the identity perimeter.

## What this proves
- I can design and document a CA baseline that is **operationally deployable** and **audit-reviewable**.
- I understand **identity attack paths** (legacy auth, risky sign-in, admin roles) and implement controls that reduce blast radius.
- I can define **exception handling** that is explicit, time-bound, and reviewable (no “forever exclusions”).

## Operating Baseline
**Assumptions (enterprise default):**
- Tenant has Microsoft Entra ID with Conditional Access available.
- MFA is supported via Microsoft Authenticator / FIDO2 / OTP (org choice).
- At least two emergency access (“break-glass”) accounts exist and are stored with controlled access.
- Administrative roles use separate admin accounts (where possible).

**Baseline objective:**
- Default-deny risky patterns, require MFA for normal access, and require stronger controls for privileged operations.

## Design
### Policy set (minimal baseline)
| Policy | Target | Control | Key settings |
| --- | --- | --- | --- |
| CA-01 Require MFA (All Users) | All users | Require MFA | Exclude break-glass only |
| CA-02 Block Legacy Auth | All users | Block | Legacy auth clients |
| CA-03 Require MFA for Admin Roles | Directory roles | Require MFA | Stronger enforcement for privileged identities |
| CA-04 Require Compliant Device (Optional) | High-risk apps | Require compliant device | Use only if device mgmt exists |
| CA-05 Risk-based Sign-in (Optional) | All users | Require MFA / block | If risk signals available |

### Exception model
**Allowed exception types**
- Break-glass accounts (emergency only)
- Service accounts / automation identities (prefer workload identities)
- Vendor/partner access (prefer B2B + scoped access)

**Exception rules**
- Must be documented (who, why, scope, expiry)
- Must be time-bound
- Must be reviewed periodically (access review cadence)

## Steps I take (only what matters)
1) **Create/validate break-glass accounts**
   - Ensure 2 accounts, unique strong credentials, stored securely.
   - Exclude from CA-01 only (not broadly excluded).

2) **Implement CA-01: Require MFA for all users**
   - Include: All users
   - Exclude: Break-glass accounts only
   - Grant: Require MFA
   - Session: Keep defaults unless business requires changes

3) **Implement CA-02: Block legacy authentication**
   - Include: All users
   - Client apps: Other clients / legacy authentication
   - Access: Block

4) **Implement CA-03: Protect privileged roles**
   - Target: Directory roles (admin roles)
   - Require MFA (and optionally require trusted locations/compliant device if available)

5) **Define exception register**
   - Document any exclusions beyond break-glass (should be rare)
   - Record: owner, justification, affected apps/users, expiry date, reviewer

## Verification
### Expected
- Normal users are prompted for MFA during interactive sign-in.
- Legacy auth attempts are blocked.
- Privileged role sign-ins are consistently protected with MFA.
- Break-glass accounts can sign in (for emergency only) and are not used day-to-day.

### Observed
- (To be captured during implementation)

## Evidence
- Evidence Index: [`./evidence/evidence-index.md`](./evidence/evidence-index.md)

**Evidence we will capture (minimum):**
- Screenshot of CA policy list showing CA-01/02/03 enabled
- Screenshot of CA-01 config (include/exclude)
- Screenshot of legacy auth block settings
- Sign-in logs showing MFA requirement applied
- Exception register entry (if any exclusions exist)

## Controls mapped
- **NIST 800-53:** AC-2, AC-6, IA-2, IA-5, AU-2, AU-12

---

## Navigation
- Repo README: [Home](../README.md)
- Pillar README: [01 — IGA](./README.md)
- Strategy Wrapper: [04 — Strategy](../04_Strategy_Risk_Resilience/README.md)
