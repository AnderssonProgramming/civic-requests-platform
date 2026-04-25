# Deliverable 3 — Development Budget

**Project:** CivicLink
**Method:** Velocity-based budgeting (Scrum)
**Currency:** USD (with COP equivalents at indicative rate)
**Date of estimate:** April 2026

---

## 1. Method

Per the workshop reference text, the budget is derived as:

```
Budget = Cost per Sprint × Number of Sprints + Tools + Equipment + Contingency
```

with effort estimated in **story points** and converted to elapsed sprints using **velocity**:

```
Number of Sprints = ⌈ Total Story Points / Velocity ⌉
```

Story points are not hours, but converted to **role-hours per sprint** using each role's allocation in the team. Hourly rates are then applied per role.

---

## 2. Inputs

| Input | Value | Source |
|---|---|---|
| Total backlog | **218 SP** | [Backlog](02-product-backlog.md) |
| Steady-state velocity | **45 SP / sprint** | Industry benchmark for a 6-dev team, validated in retrospectives |
| Sprint length | **2 weeks** (10 working days, 80 working hours per FTE) | Standard Scrum |
| Number of sprints | **⌈218 / 45⌉ = 5** | Computed |
| Project duration | **10 weeks** (+1-week Sprint 0 for setup) | Computed |
| Team FTE composition | 7 roles, mixed allocation | Section 3 |

---

## 3. Team and Allocations

| Role | Allocation | Hours over 10 weeks | Why this allocation |
|---|---|---|---|
| Project Manager | 60% | 240 | Ceremonies, stakeholder mgmt, budget tracking — not hands-on coding |
| Tech Lead / Solution Architect | 100% | 400 | Architecture, code reviews, mentoring, hardest stories |
| Frontend Developer #1 | 100% | 400 | Citizen Portal |
| Frontend Developer #2 | 100% | 400 | Admin Dashboard |
| Backend Developer #1 | 100% | 400 | requests-service, departments-service |
| Backend Developer #2 | 100% | 400 | identity-service, notifications-service, reports-service |
| DevOps Engineer | 80% | 320 | CI/CD, infra, observability, release engineering |
| QA Engineer | 100% | 400 | Test plans, automation, UAT support |
| UX/UI Designer | 50% | 200 | Front-loaded in Sprints 0–2, lighter from Sprint 3 |
| **Total** | — | **3,160** | |

> *Note.* The PM, Tech Lead, DevOps, QA, and UX roles can be staffed by more than one person at lower allocations — the totals (hours and cost) are what matter for the budget.

---

## 4. Hourly Rates (Colombian market, 2026)

Rates are blended (mid + senior) and consistent with public salary surveys for Colombia. They are **fully loaded** (gross salary + social contributions + overhead).

| Role | Hourly Rate (USD) | Hourly Rate (COP @ 4,200) |
|---|---|---|
| Project Manager | $40 | $168,000 |
| Tech Lead / Solution Architect | $60 | $252,000 |
| Frontend Developer (blended) | $35 | $147,000 |
| Backend Developer (blended) | $38 | $159,600 |
| DevOps Engineer | $45 | $189,000 |
| QA Engineer | $28 | $117,600 |
| UX/UI Designer | $35 | $147,000 |

---

## 5. Labor Cost Breakdown

| Role | Hours | Rate (USD) | Cost (USD) |
|---|---:|---:|---:|
| Project Manager (60%) | 240 | $40 | $9,600 |
| Tech Lead / Architect | 400 | $60 | $24,000 |
| Frontend Dev #1 | 400 | $35 | $14,000 |
| Frontend Dev #2 | 400 | $35 | $14,000 |
| Backend Dev #1 | 400 | $38 | $15,200 |
| Backend Dev #2 | 400 | $38 | $15,200 |
| DevOps Engineer (80%) | 320 | $45 | $14,400 |
| QA Engineer | 400 | $28 | $11,200 |
| UX/UI Designer (50%) | 200 | $35 | $7,000 |
| **Subtotal labor** | **3,160** | | **$124,600** |

---

## 6. Other Costs

### 6.1 Tools and Licenses (10 weeks)

| Item | Tier | Cost (USD) |
|---|---|---|
| GitHub Team | Per seat × 9 | $200 |
| Auth0 Essentials | Up to 1k MAUs | $500 |
| Atlassian Jira + Confluence | 10 seats | $300 |
| Figma | 3 editor seats | $150 |
| Sentry Team | 1 organization | $300 |
| Datadog / Grafana Cloud Pro | 5 hosts | $500 |
| AWS dev + staging (compute, RDS, S3, MSK basic, CloudWatch) | mixed | $2,500 |
| Domains, SSL, miscellaneous | — | $200 |
| **Subtotal** | | **$4,650** |

### 6.2 Equipment and Onboarding

| Item | Cost (USD) |
|---|---|
| Hardware top-up / peripherals (3 × $500 average) | $1,500 |
| Onboarding, training material, kickoff workshop | $500 |
| **Subtotal** | **$2,000** |

### 6.3 Contingency Reserve

15% of (labor + tools + equipment) = 0.15 × ($124,600 + $4,650 + $2,000) = **$19,688**.

Contingency covers: scope creep on the **Could** epic (E8), velocity dips during the first sprint, surprises in the Carpeta Ciudadana integration, and minor rate variations.

---

## 7. Total Project Cost

| Category | Amount (USD) | Amount (COP @ 4,200) |
|---|---:|---:|
| Labor | $124,600 | COP 523,320,000 |
| Tools & licenses | $4,650 | COP 19,530,000 |
| Equipment & onboarding | $2,000 | COP 8,400,000 |
| Contingency (15%) | $19,688 | COP 82,689,600 |
| **Total (point estimate)** | **$150,938** | **~ COP 633,940,000** |

### 7.1 Range (sensitivity)

Applying ±15% to capture rate volatility, velocity uncertainty, and scope drift:

| Scenario | Total (USD) | Total (COP) |
|---|---:|---:|
| **Optimistic (P10)** | **$128,300** | COP 538,860,000 |
| **Likely (P50)** | **$150,938** | COP 633,940,000 |
| **Pessimistic (P90)** | **$173,580** | COP 729,030,000 |

### 7.2 Cost per Sprint

```
Cost per Sprint ≈ $124,600 / 5 = $24,920 (labor only)
Fully loaded per sprint ≈ $150,938 / 5 = $30,188
```

This means each sprint delivers ≈ 45 SP for ~$30k → **~$670 per story point** (fully loaded). Useful for change requests: a new 5 SP story costs roughly $3,350.

---

## 8. Sensitivity and Trade-offs

| Lever | Impact |
|---|---|
| Drop the **Could** epic (E8, 21 SP) | Saves ~$14,000 (≈ half a sprint) |
| Cut UX/UI from 50% to 25% | Saves $3,500 but risks usability |
| Replace one Senior dev with a Mid dev (-$10/h) | Saves ~$4,000, possibly +1 sprint |
| Add a sixth sprint for hardening | +$30k, raises confidence to ~95% |
| Move from EKS managed control plane to self-hosted K3s | Saves ~$700 in cloud, adds DevOps load |

---

## 9. Assumptions

1. **Team is fully staffed from day one** of Sprint 1; Sprint 0 is shared across roles and budgeted within the labor totals.
2. **Velocity stabilises at 45 SP** by Sprint 2; Sprint 1 plans for ~45 with low buffer because the team is experienced.
3. **No travel costs**; team is co-located in Bogotá or fully remote with daily overlap.
4. **Production operations are out of scope** of this project budget. Running CivicLink in production is a separate operations budget owned by the municipality.
5. **Auth0 Essentials tier** is sufficient for the build phase. Production volume might require a larger plan.
6. **Government SSO integration** (US-42) requires no paid integration — only OIDC config — and is treated as a Could.
7. **Hourly rates** reflect the Colombian market in 2026; mid+senior blend.
8. **Photo storage at MVP scale** stays under 50 GB — S3 cost is negligible (<$10/month) and is bundled in the cloud line.

---

## 10. Risk Register (cost-relevant)

| ID | Risk | Likelihood | Impact (USD) | Mitigation |
|---|---|---|---:|---|
| R1 | Carpeta Ciudadana integration delayed or paid | Medium | +$8,000 | Treated as Could; buffered |
| R2 | Velocity dips below 35 SP for 2 sprints | Medium | +$25,000 | Buffer + scope re-prioritisation |
| R3 | A senior dev leaves mid-project | Low | +$10,000 | Tech Lead absorbs; +1 sprint |
| R4 | Cloud cost spike (load tests in staging) | Low | +$2,000 | Rate-limit load tests, schedule off-hours |
| R5 | Auth0 needs Professional plan early | Low | +$1,500 | Cap MAUs; switch tier if needed |
| R6 | Currency volatility (COP/USD) | Medium | ±10% | Lock contracts in COP for local team |
| R7 | Scope creep from stakeholders | High | +$15,000 | MoSCoW + change-request priced at $670/SP |

---

## 11. Acceptance of the Estimate

This budget is presented as a **fixed-time, scoped backlog** plan: the timeline (10 weeks + 1 setup) and the **Must** scope are committed; **Should** is expected; **Could** is conditional. If the municipality fixes the budget instead of the scope, the team will commit only the **Must** epics first and prioritise **Should** until budget is exhausted, in line with Scrum's *fixed-budget* mode described in the workshop reference.

---

## 12. Quick Reference

| Question | Answer |
|---|---|
| How long? | 10 weeks (5 sprints × 2 weeks) + 1 week Sprint 0 |
| How big a team? | 7 roles, 3,160 total hours |
| How much? | **USD $150,938** point estimate, **$128k – $174k** range |
| Per sprint? | ~$30,188 fully loaded |
| Per story point? | ~$670 fully loaded |
| What's not included? | Production operations, third-party SaaS production tiers, marketing |