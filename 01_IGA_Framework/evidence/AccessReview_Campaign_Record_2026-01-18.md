## Access Review Campaign Record — 2026-01-18 (Manual Certification)

![Status: COMPLETE](https://img.shields.io/badge/Status-COMPLETE-198754?style=for-the-badge)
![Change Policy: IMMUTABLE](https://img.shields.io/badge/Change%20Policy-IMMUTABLE-212529?style=for-the-badge)
![Framework: NIST 800-53](https://img.shields.io/badge/Framework-NIST%20800--53-0d6efd?style=for-the-badge)
![Audience: Recruiters/Auditors](https://img.shields.io/badge/Audience-Recruiters%20%2F%20Auditors-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** This campaign record is **IMMUTABLE**. Future certifications must be recorded in a new dated record (supersede; do not edit).

---

## Campaign Metadata
| Field | Value |
| --- | --- |
| Campaign ID | AR-2026-01-18 |
| Review Type | Manual certification (license-constrained) |
| Review Window | 2026-01-18 |
| Tenant Constraint | Entra Access Reviews requires P2/EMS E5; not available in this tenant |
| Reviewer | Robert Myers |
| Approval Authority | Role Owner = Robert Myers (Tenant Admin); Governance Owner = Robert Myers |
| Default Action | Remove access if not approved / no response (per SOP) |

---

## Evidence (linked)
| Evidence ID | Artifact | What it proves |
| --- | --- | --- |
| EV-2026-01-18-001 | [Access Reviews license gate](./EV-2026-01-18-001_access_reviews_license_gate.png) | Automation is license-gated; compensating control required |
| EV-2026-01-18-002 | [Roles scope defined](./EV-2026-01-18-002_roles_scope_defined.png) | Review scope defined (privileged directory roles) |
| EV-2026-01-18-003 | [Global Admin assignments](./EV-2026-01-18-003_role_assignments_global_admin.png) | Baseline: Global Administrator membership |
| EV-2026-01-18-004 | [Privileged Role Admin assignments](./EV-2026-01-18-004_role_assignments_privileged_role_admin.png) | Baseline: Privileged Role Administrator membership |
| EV-2026-01-18-005 | [Security Admin assignments](./EV-2026-01-18-005_role_assignments_security_admin.png) | Baseline: Security Administrator membership |

---

## Review Scope (Privileged Roles)
| Role | Included | Notes |
| --- | --- | --- |
| Global Administrator | Yes | Review current assignments |
| Privileged Role Administrator | Yes | Review current assignments |
| Security Administrator | Yes | Review current assignments |

---

## Decision Record (Certification Results)

> **Owner/Approver standard (small-tenant reality):** Role Owner = Tenant Admin (you) and Governance Owner = you (acting as governance). In enterprise, this would be a separate identity governance owner.

### Global Administrator
| Account / UPN | Access Needed? | Decision | Owner/Approver | Rationale | Due (if removal) |
| --- | --- | --- | --- | --- | --- |
| BG-Admin-01 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Break-glass identity #1 required for emergency access; not used for daily operations | N/A |
| bg-admin-02 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Break-glass identity #2 required for emergency access redundancy | N/A |
| Robert Myers | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Primary administrative identity required for tenant operations | N/A |

### Privileged Role Administrator
| Account / UPN | Access Needed? | Decision | Owner/Approver | Rationale | Due (if removal) |
| --- | --- | --- | --- | --- | --- |
| BG-Admin-01 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Break-glass must retain ability to recover role administration in incident conditions | N/A |
| bg-admin-02 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Redundant emergency identity for privileged role recovery | N/A |
| Robert Myers | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Operational need: role administration in small-tenant model | N/A |

### Security Administrator
| Account / UPN | Access Needed? | Decision | Owner/Approver | Rationale | Due (if removal) |
| --- | --- | --- | --- | --- | --- |
| BG-Admin-01 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Break-glass identity required to restore security controls during incident response | N/A |
| bg-admin-02 | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Redundant emergency identity for security control recovery | N/A |
| Robert Myers | Yes | Retain | Robert Myers (Tenant Admin / Governance) | Required for tenant security configuration and monitoring | N/A |

---

## Remediation Actions (If Any Deny/Remove)
| Item | Action | SLA | Status | Evidence |
| --- | --- | --- | --- | --- |
| R-01 | Remove role assignment for N/A | T+24h | N/A | N/A |
| R-02 | Incident opened (if SLA breached) | T+24h | N/A | N/A |

---

## Exceptions (If Any)
- **Exception Register:** `../../EXCEPTION_REGISTER.md`
- Entries created: **NO**
- If YES, list Exception IDs: N/A

---

## Remediation Loop (Control Requirement)
If any future certification results in **Remove**:
- removal must occur within **T+24h**
- capture:
  - post-change role assignment view
  - audit log entry “Remove member from role”
- if not removed within **T+24h**, open an incident and follow escalation.

### Escalation Path (Minimal)
- **T+24h:** Incident Report opened; owner notified.
- **T+48h:** Escalate to Governance lead / Security lead.
- **T+72h:** Leadership notification (for privileged roles).

---

## Completed
- Campaign completed on: **2026-01-18**
- Outcome summary: **No removals required; baseline validated**

---

## Navigation
- SOP: [`../Access_Review_SOP.md`](../Access_Review_SOP.md)
- Evidence index: [`./evidence-index.md`](./evidence-index.md)
- Exception register: [`../../EXCEPTION_REGISTER.md`](../../EXCEPTION_REGISTER.md)

