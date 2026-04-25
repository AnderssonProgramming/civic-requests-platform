# User Story Map — CivicLink

User story mapping organises the backlog around the **user journey** (horizontal backbone) and **release slices** (vertical layers). It complements the flat backlog by making *what each release ships to whom* visible at a glance.

The backbone reads like the citizen's narrative: **Discover → Sign in → Submit → Track → Communicate → Get resolved → Be heard**.

---

## 1. Two-axis Map

```
┌──────────────────────────────────────────────────────────────────────────────────────────┐
│                                  USER ACTIVITIES (Backbone)                              │
├────────────┬──────────┬──────────────┬──────────┬──────────────┬─────────────┬───────────┤
│  Discover  │  Sign in │   Submit     │  Track   │ Communicate  │ Resolution  │ Be heard  │
└────────────┴──────────┴──────────────┴──────────┴──────────────┴─────────────┴───────────┘

╔════════════════════════════════ RELEASE 1 — MVP (Sprint 1–3) ═══════════════════════════╗
║ Land page  │ Email/pwd │ Title+desc   │ My list  │ —            │ Status      │ —      ║
║ About PQRS │ Google    │ Category     │ Status   │              │ change      │        ║
║            │ Verify    │ Photos       │ Timeline │              │             │        ║
║            │ Reset     │ Geolocation  │ Public   │              │             │        ║
║            │           │ Tracking ID  │ link     │              │             │        ║
║            │           │ Drafts       │          │              │             │        ║
╠══════════════════════════════ RELEASE 2 — VALUE (Sprint 4) ═════════════════════════════╣
║            │ Profile   │ Anonymous    │ Filters  │ Citizen→Staff│ Assignment  │        ║
║            │ edit      │ submission   │ Search   │ Staff→Citizen│ Internal    │        ║
║            │           │              │ Dept info│ Reply alerts │ notes       │        ║
║            │           │              │          │              │ Escalation  │        ║
║            │           │              │          │              │ Roles       │        ║
║            │           │              │          │              │ Departments │        ║
╠══════════════════════════════ RELEASE 3 — INSIGHT (Sprint 5) ═══════════════════════════╣
║ Public     │ —         │ —            │          │ Rating       │             │ KPI    ║
║ trans-     │           │              │          │ on close     │             │ dashbd ║
║ parency    │           │              │          │              │             │ Dept   ║
║ portal     │           │              │          │              │             │ perf   ║
║            │           │              │          │              │             │ Heatmap║
║            │           │              │          │              │             │ Export ║
╠══════════════════════════ RELEASE 4 — INTEGRATIONS (post-launch) ═══════════════════════╣
║            │ Carpeta   │ —            │          │              │             │ Open   ║
║            │ Ciudadana │              │          │              │             │ data   ║
║            │ SSO       │              │          │              │             │ API    ║
║            │           │              │          │              │             │ Webhook║
║            │           │              │          │              │             │ GIS    ║
╚══════════════════════════════════════════════════════════════════════════════════════════╝
```

---

## 2. Backbone × User Stories

| Activity | Release 1 (MVP) | Release 2 (Value) | Release 3 (Insight) | Release 4 (Integrations) |
|---|---|---|---|---|
| **Discover** | Landing + About | — | Public transparency portal (US-37) | — |
| **Sign in** | US-01, US-02, US-03, US-04, US-06 | US-05 | — | US-42 |
| **Submit** | US-07, US-08, US-09, US-10, US-12, US-13, US-14 | US-11 | — | — |
| **Track** | US-15, US-16, US-17, US-19 | US-18, US-20 | — | — |
| **Communicate** | — | US-21, US-22, US-23 | US-24 | — |
| **Resolution** | US-28, US-38 | US-27, US-29, US-30, US-31, US-32, US-39, US-40, US-41 | — | US-43, US-45 |
| **Be heard** | — | US-25, US-26 | US-33, US-34, US-35, US-36 | US-44 |
| **Platform / NFR** | US-46, US-47, US-48, US-50, US-51 | US-49 | — | — |

---

## 3. Reading the Map

**Read across (the backbone)** to see the citizen's full journey at any release. Even Release 1 contains every backbone activity except *Communicate* and *Be heard*, which means the MVP delivers an end-to-end "submit → track → resolve" loop — a real release, not a demo.

**Read down (each column)** to see how an activity grows over releases. *Submit*, for example, gets richer over time without changing the user's mental model.

**Use the map to negotiate.** If the budget shrinks, drop the **bottom row** (Release 4) — every Activity above it still tells a complete story. This is the central virtue of mapping over a flat backlog: cuts are visible and humane.