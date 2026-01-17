# Savings Cases (Rightsizing + Storage Tiering)

![Status: DRAFT](https://img.shields.io/badge/Status-DRAFT-6c757d?style=for-the-badge)
![Framework: FinOps](https://img.shields.io/badge/Framework-FinOps-0d6efd?style=for-the-badge)
![Audience: Recruiters/Auditors](https://img.shields.io/badge/Audience-Recruiters%20%2F%20Auditors-212529?style=for-the-badge)

> [!IMPORTANT]
> **Governance Change Policy:** Once marked **COMPLETE**, these savings cases are **IMMUTABLE**. Any change requires updated analysis, approval, and revised savings evidence.

---

## Strategic Goal
Demonstrate measurable cloud cost optimization through **repeatable savings cases** that reduce waste without introducing operational risk.

These cases show how governance, not ad-hoc tuning, drives sustainable cost reduction.

---

## What This Proves
- I identify waste using data, not intuition.
- I evaluate savings through risk-aware analysis.
- I document expected vs. realized savings.
- I align technical optimization with financial accountability.

---

## Governance Decisions
- Savings actions are driven by data (usage, trends, baselines).
- Changes are scoped, reversible, and validated post-change.
- Savings are reported as **forecasted vs. realized**.
- High-risk changes require approval and rollback planning.
- One-time savings are distinguished from recurring savings.

---

## Scope & Non-Goals
| In scope | Out of scope (by design) |
| --- | --- |
| Compute rightsizing | Application refactoring |
| Storage tier optimization | Data deletion strategies |
| Savings measurement | Vendor discount negotiations |
| Evidence capture | Fully automated optimization tools |

---

## Savings Case 1 — Compute Rightsizing

### Problem Statement
Compute resources were provisioned above actual utilization, resulting in sustained underused capacity and unnecessary monthly spend.

---

### Analysis
| Metric | Observed |
| --- | --- |
| Average CPU utilization | < 20% |
| Memory utilization | < 30% |
| Instance size | DS3_v2 |
| Runtime profile | Steady-state |

Rightsizing candidate identified through usage metrics and trend stability.

---

### Action
- Resize DS3_v2 → DS2_v2
- Validate workload performance post-change
- Monitor utilization and error rates

---

### Financial Impact
| Item | Value |
| --- | --- |
| Monthly cost (before) | $X |
| Monthly cost (after) | $Y |
| Monthly savings | $X − $Y |
| Annualized savings | ($X − $Y) × 12 |

Savings type: **Recurring**

---

### Risk & Controls
| Risk | Mitigation |
| --- | --- |
| Performance degradation | Monitor metrics + rollback |
| Capacity spike | Alert thresholds |
| User impact | Maintenance window |

---

### Verification
**Expected**
- Utilization increases to target range (40–70%).
- No performance regression.

**Observed**
- Captured post-change and retained as evidence.

---

## Savings Case 2 — Storage Tiering

### Problem Statement
Large volumes of infrequently accessed data were retained in hot storage tiers, driving unnecessary storage cost.

---

### Analysis
| Metric | Observed |
| --- | --- |
| Access frequency | < 1x / 90 days |
| Storage tier | Hot |
| Data classification | Non-critical |

---

### Action
- Move eligible data from Hot → Cool / Archive tiers
- Apply lifecycle management policy
- Validate retrieval path

---

### Financial Impact
| Item | Value |
| --- | --- |
| Monthly cost (before) | $X |
| Monthly cost (after) | $Y |
| Monthly savings | $X − $Y |
| Annualized savings | ($X − $Y) × 12 |

Savings type: **Recurring**

---

### Risk & Controls
| Risk | Mitigation |
| --- | --- |
| Retrieval latency | Document SLA |
| Data loss | Backup validation |
| Compliance impact | Data classification review |

---

### Verification
**Expected**
- Storage cost reduced.
- Data remains retrievable within SLA.

**Observed**
- Captured post-change and retained as evidence.

---

## Savings Summary
| Case | Savings Type | Monthly | Annual |
| --- | --- | ---: | ---: |
| Compute rightsizing | Recurring | $ | $ |
| Storage tiering | Recurring | $ | $ |
| **Total** | — | $ | $ |

---

## Audit Tests

### Test of Design
- [ ] Savings methodology is documented.
- [ ] Risk assessment exists for each case.
- [ ] Approval path is defined.
- [ ] Measurement approach is consistent.

### Test of Effectiveness
- [ ] Cost reduction visible in billing data.
- [ ] Savings persist beyond one billing cycle.
- [ ] No service degradation observed.
- [ ] Evidence retained for audit review.

---

## Evidence
Evidence Index: `./evidence/evidence-index.md`

Minimum artifacts:
- EV-YYYY-MM-DD-001 — Usage analysis snapshot
- EV-YYYY-MM-DD-002 — Change implementation proof
- EV-YYYY-MM-DD-003 — Post-change cost comparison
- EV-YYYY-MM-DD-004 — Risk/approval record

---

## Controls Mapped
- FinOps Framework: Optimization, Efficiency, Value Realization

---

## Navigation
- Repo README: `../README.md`
- Pillar README: `./README.md`
- Related Packs:
  - `./Monthly_Showback_Template.md`
  - `./Budget_Alert_Thresholds.md`
