# Screenshot Naming Standard

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Audience: Recruiters/Auditors](https://img.shields.io/badge/Audience-Recruiters%20%2F%20Auditors-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** Naming is **IMMUTABLE** once adopted. Evidence IDs must remain stable so links and audit trails do not break.

---

## Purpose
Ensure evidence screenshots are sortable, traceable, and consistent across all proof packs.

---

## Required Naming Format
`EV-YYYY-MM-DD-###_<pillar>_<pack>_<what>.png`

Examples:
- `EV-2026-01-20-001_iga_ca_ca02_policy_enabled.png`
- `EV-2026-01-20-002_iga_pim_activation_settings.png`
- `EV-2026-01-20-003_finops_budget_thresholds_config.png`

---

## Placement
Screenshots live under the pillar evidence folder:
- `01_IGA_Framework/evidence/screenshots/`
- `02_Cloud_Guardrails/evidence/screenshots/`
- `03_FinOps_Governance/evidence/screenshots/`
- `04_Strategy_Risk_Resilience/evidence/screenshots/` (rare)

---

## Evidence ID Rules
- Format: `EV-YYYY-MM-DD-###`
- `###` increments per day (001, 002, 003…)
- Evidence ID must appear in the pillar’s `evidence/evidence-index.md`

---

## Sanitization Rules (before upload)
Remove/blur:
- tenant name, subscription IDs, domains
- user identities (UPN/email/name)
- resource names that reveal organizational context
- IPs, locations, unique identifiers
- secrets/keys/tokens

Use placeholders in text:
- `[REDACTED_TENANT]`
- `[REDACTED_SUBSCRIPTION]`
- `[REDACTED_USER]`
- `[REDACTED_RESOURCE]`

---

## Capture Standard
- Capture only what proves the claim.
- Prefer configuration views over dashboards.
- If a control spans multiple areas, capture multiple screenshots and sequence EV IDs.
