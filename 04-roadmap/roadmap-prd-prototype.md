# Roadmap, PRD & Prototype

> **Module 4 · ★ Deliverable 4.** Repo file `04-roadmap/roadmap-prd-prototype.md` — part of your submission.
> Do the lab in the **Module 4 · Exercise 1 Guide** (linked from the Module 4 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Roadmap, PRD & Prototype** slide of your Module 6 final deck. (Your Module 4 · Exercise 2 PRD sprint lands in `prd-and-prototype.md`.)

## High-level product roadmap

_Future direction, key milestones, and phased execution over time._

Velocity closes the coordinator's assignment loop in two phases: first the re-route, then compliance. Interactive version: [`roadmap.html`](roadmap.html).

| Lane | Features | Why |
|---|---|---|
| **NOW** · Pilot (4 weeks, 3 accounts) | B6 Driver Alert Notifications · B5 Step Progress Indicator | Quick Wins: B6 kills the moment of misery (a re-route takes 8–15 min to reach the driver, BUG-2044); B5 targets abandonment after assignment (91% open the board, 18% finish) |
| **NEXT** · GA (weeks 5–8) | B1 One-Click Compliance Checklist · B4 Mobile-First Coordinator Dashboard | B1 is the largest measured gap (14.6 vs 3.0 min, drop-off 71% → 48%) but too big to build next to B6 with 2 engineers; B4 builds on both |
| **LATER** · Backlog | B9 Compliance Audit Trail Export · B10 In-App Coordinator Training | B9 only matters once B1 captures compliance data; the CS lead onboards the pilot accounts by hand |
| **CUT** | B2 Daily Report Auto-Fill · B3 Shift Handoff Wizard · B7 AI ETA Display · B8 Fleet Analytics Manager View | Outside the loop, low adoption (B7: 11%), or Sales-driven (B8); B2 also puts the Reporting guardrail at risk |

**Milestones:** week 4, the pilot passes the PRD evals and moves to GA · week 8, go/no-go on in-tool completion (scale at ≥ 30%, target 36%, guardrail ≥ 4.3).

**Scoring:** Effort vs. Value (1–5), constrained by 2 engineers, 1 designer and 1 CS lead. I favoured the coordinator's core friction over Sales, Legal and CS requests.

## PRD snippets

_The key elements of your simplified PRD._

**Feature:** B6 Driver Alert Notifications. Full PRD: [`prd-b6-driver-alerts.md`](prd-b6-driver-alerts.md).

- **Vision:** A re-route reaches the driver in seconds and is confirmed in one tap, so the coordinator never has to send it again on WhatsApp.
- **Must-haves:** push on re-route (≤ 5 s vs. 8–15 min today) · deep link to the updated route · one-tap confirm · Sent / Delivered / Confirmed on the board · event logging.
- **Won't (now):** compliance flag alerts (they wait for B1) · WhatsApp integration · manager notifications.
- **Safety guard:** the alert text comes only from the route record; if the stop has no address, the alert is blocked.
- **Metrics:** primary = in-tool workflow completion 18% → 36%; guardrail = Managers × Reporting CSAT ≥ 4.3.
- **Evals:** 100% of alerts match the route record · send → confirmed ≤ 30 s · 100% of unconfirmed re-routes flagged at 2 min.

## Wireframes / prototype

_A visual or interactive model of your proposed solution._

Working prototype: [`prototype-b6-driver-alerts.html`](prototype-b6-driver-alerts.html). Open it in any browser.

It has three screens: the Live Dispatch board (entry point), the driver's phone with the alert and the new route (feature core), and the board's _Confirmed in 0:xx_ status (success). It also includes 6 walkthrough scenarios: happy path, no signal, conflicting changes, the safety guard, an unassigned route, and a cancelled change.
