# Evidence Standards

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Audience: Recruiters/Auditors](https://img.shields.io/badge/Audience-Recruiters%20%2F%20Auditors-212529?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** Once a proof pack is marked **COMPLETE**, its evidence structure is **IMMUTABLE**. Any change requires documented justification, updated index entries, and (if applicable) a Risk Acceptance entry.

---

## Purpose
Define what qualifies as evidence in this repository and how artifacts are retained, referenced, and reviewed.

This repository is an evidence library:
- documents describe **design intent**
- evidence proves **implementation and operational reality**

---

## Evidence Rules

### Sanitization (required)
- No tenant IDs, subscription IDs, UPNs/emails, personal names, secret values, internal hostnames, or public IPs.
- Use `[REDACTED]` consistently.

### Traceability (required)
Every artifact must include:
- Evidence ID
- capture date
- source (portal blade, export, query, audit log)
- file path link from an evidence index

### Audit defensibility (required)
Artifacts must support:
- **Test of Design**: control exists and matches documented configuration
- **Test of Effectiveness**: logs/events prove enforcement or operation

### Stability (required)
Once COMPLETE:
- evidence index becomes the source of truth
- new evidence is additive, not restructuring
- exceptions require documented approval and expiration

---

## Allowed Evidence Types
- Portal screenshots (sanitized)
- Exports (sanitized)
- KQL query + results (sanitized)
- Audit / activity logs (sanitized)
- Configuration snapshots (sanitized)

---

## Required Structure (per proof pack)
Each pack maintains an `evidence/` folder containing:
- `evidence-index.md`
- `screenshots/` (optional)
- `exports/` (optional)
- `queries/` (optional)

---

## Evidence Index Entry Standard
Each entry should include:
- Evidence ID (`EV-YYYY-MM-DD-###`)
- Control claim (what it proves)
- Source
- Artifact link
- Observed (what the screenshot/export shows)
- Notes (sanitization, assumptions)

---

## Scope Note
This repository demonstrates governance patterns in a lab/personal environment.
It does not claim production authority over any employer tenant.
