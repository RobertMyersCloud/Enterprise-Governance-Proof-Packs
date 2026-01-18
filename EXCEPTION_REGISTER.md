# Exception Register

![Status: ACTIVE](https://img.shields.io/badge/Status-ACTIVE-0d6efd?style=for-the-badge)

---

## Purpose
This register documents **approved deviations** from IMMUTABLE governance baselines.  
Any exception **must be time-bound, justified, and reviewed**.

No exception may be implemented without:
- documented risk acceptance
- explicit scope
- expiration date

---

## Exception Policy
- All IMMUTABLE baselines require a Risk Acceptance (RA) for deviation
- Exceptions **must expire**
- Emergency use does **not** waive documentation

---

## Active Exceptions

> **None**

As of the last review, there are **no approved exceptions** to Identity Governance baselines.

---

## Recorded Constraints (Non-Exception)

The following are **documented environmental constraints**, not exceptions:

| Area | Description | Handling |
| --- | --- | --- |
| Conditional Access | Entra ID Premium licensing not present | Baseline implemented using Security Defaults + Auth Methods Policy |
| MFA Reporting | Advanced MFA registration reporting premium-gated | Constraint documented with evidence |
| CA Targeting | Risk / device / app-based CA unavailable | Explicitly declared out-of-scope |

These constraints are **not treated as exceptions** because:
- They do not bypass controls
- They are transparently documented
- No compensating controls are misrepresented

---

## Review Cadence
- Reviewed quarterly
- Reviewed after any baseline change request
- Reviewed after emergency access usage

---

## Navigation
- Identity Governance Evidence: `./01_IGA_Framework/evidence/evidence-index.md`
- Conditional Access Baseline: `./01_IGA_Framework/Conditional_Access_Baseline.md`
