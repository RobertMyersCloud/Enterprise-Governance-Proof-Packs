# ⭐ Conditional Access Baseline (MFA + Break-Glass + Exceptions)
> **Status:** DRAFT • **Audience:** Recruiters / Hiring Managers / Auditors • **Scope:** Entra ID (Azure-first)  
> **Change policy:** IMMUTABLE once COMPLETE

---

## Goal
Establish a defensible Conditional Access (CA) baseline that enforces strong authentication for interactive users, protects privileged identity paths, and governs exceptions explicitly—without introducing hidden bypasses or operational fragility.

This baseline is designed to survive both **real-world incidents** and **formal audit review**.

---

## What this proves
- I design Conditional Access as a **governance control**, not a collection of ad-hoc policies.
- I understand identity-based attack paths (legacy auth, admin compromise, exception sprawl) and reduce them systematically.
- I implement **controlled emergency access** (break-glass) without weakening the identity perimeter.
- I document CA controls in a way that supports **test of design** and **test of effectiveness**.

---

## Scope & Non-Goals
**In scope**
- Interactive user authentication
- Privileged role sign-ins
- Emergency access (break-glass) governance
- Exception documentation and review

**Out of scope (by design)**
- Device compliance enforcement (requires managed endpoint baseline)
- Continuous access evaluation tuning
- App-level sign-in risk policies requiring premium telemetry

These are intentionally excluded to keep the baseline **deployable in most enterprises**.

---

## Governance Decisions (why this design)
- Break-glass accounts are excluded **only** from the global MFA policy to preserve emergency access without broad CA bypass.
- Legacy authentication is blocked tenant-wide to eliminate downgrade attack paths; exceptions require formal risk acceptance.
- Privileged roles are treated as **high-consequence identities** and receive stricter enforcement.
- Exceptions are governed as **temporary risk decisions**, not permanent technical shortcuts.

---

## Operating Baseline
**Enterprise assumptions**
- Microsoft Entra ID tenant with Conditional Access available
- MFA methods defined and supported by the organization
- At least two emergency access accounts exist
- Administrative roles use separate admin identities where feasible

**Baseline objective**
- Enforce MFA everywhere it matters
- Eliminate legacy auth
- Reduce blast radius of privileged compromise
- Make all exceptions visible, reviewable, and reversible

---

## Design
### Conditional Access policy set
| Policy ID | Policy Name | Target | Control |
| --- | --- | --- | --- |
| CA-01 | Require MFA – All Users | All users | Require MFA |
| CA-02 | Block Legacy Authentication | All users | Block |
| CA-03 | Protect Privileged Roles | Directory roles | Require MFA |
| CA-04 | Risk-Based Controls (Optional) | All users | Require MFA / Block |

### Exception model
**Permitted exception types**
- Break-glass emergency accounts
- Service or automation identities (prefer workload identities)
- Vendor or partner access (prefer B2B with scoped access)

**Exception requirements**
- Documented justification
- Explicit scope (who/what)
- Time-bound expiration
- Periodic review cadence

---

## Steps I take (only what matters)
1. **Validate emergency access**
   - Confirm two break-glass accounts exist
   - Secure credentials offline
   - Exclude from CA-01 only

2. **Implement CA-01 (Require MFA – All Users)**
   - Include: All users
   - Exclude: Break-glass only
   - Grant: Require MFA

3. **Implement CA-02 (Block legacy authentication)**
   - Include: All users
   - Client apps: Legacy authentication
   - Access: Block

4. **Implement CA-03 (Privileged role protection)**
   - Target: Directory roles
   - Require MFA consistently

5. **Establish exception register**
   - Record owner, justification, scope, expiration
   - Align with access review cadence

---

## Audit Tests
**Test of Design**
- Conditional Access policies exist, are enabled, and match documented scope and exclusions.

**Test of Effectiveness**
- Sign-in logs show MFA enforced for interactive access.
- Legacy authentication attempts are blocked.
- Privileged sign-ins consistently require MFA.

---

## Verification
**Expected**
- MFA prompts for interactive sign-ins
- Legacy auth blocked tenant-wide
- Privileged role
