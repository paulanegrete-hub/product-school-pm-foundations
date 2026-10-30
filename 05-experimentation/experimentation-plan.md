# Experimentation Plan (Module 5)

> **Module 5 · ★ Deliverable 5.** Repo file `05-experimentation/experimentation-plan.md` — part of your submission.
> It becomes the **Experimentation Plan** slide of your Module 6 final deck.

## Overview

A 4-week, 50/50 A/B test of **B6 Driver Alerts** alone, randomized by dispatch team inside the 3 pilot accounts. It tests the re-route half of the coordinator's assignment loop before the compliance half (B1) ships. If B6 lifts in-tool workflow completion to the 30% floor without hurting Manager Reporting CSAT, it ships. If it lifts completion but stays below the floor, B6 stays and the next test adds B1.

## What you're testing

| Element | Detail |
|---|---|
| Hypothesis under test | Pushing a re-route straight to the driver, confirmed in one tap (B6), lifts in-tool daily workflow completion from 18% to at least 30%, because coordinators no longer need WhatsApp to close the re-route loop |
| Experiment design (A/B, etc.) | A/B, 50/50 by dispatch team inside the 3 pilot accounts, 4 weeks, ~198 coordinator-days per arm |
| Primary metric | % of coordinators completing the daily dispatch workflow in-tool (baseline 18%, MDE +12 pp) |
| Guardrail metric | Managers × Reporting CSAT ≥ 4.3 (today 4.5) |
| Decision rule (ship / kill / pivot) | Ship if B ≥ 30%, p < 0.05 and the guardrail holds · pivot (keep B6, test B6 + B1) if B wins but stays below 30% · kill or roll back if there's no lift or the guardrail breaks |

## Get your documents ready

- **From M3, your hypothesis sentence:** Based on dispatchers running the day from a WhatsApp group (UXR-02) and only 18% of coordinators finishing their daily workflow in RouteLogic, I believe that a focused Velocity workspace that closes the assignment loop (the re-route reaches the driver in seconds and compliance is logged in the same flow) will move coordinators back into RouteLogic and reduce complexity-driven churn, as measured by a 2× increase in in-tool workflow completion (18% → 36%). I will protect Manager Reporting CSAT (≥ 4.3) and make a go/no-go decision at week 8.
- **From M3, your primary success metric & guardrail metric:** Primary: in-tool daily workflow completion among coordinators, 18% → 36%. Guardrail: Managers × Reporting CSAT ≥ 4.3 (today 4.5).
- **From M4, the feature you scoped in your PRD (this is what you're testing):** B6 Driver Alerts. The re-route is pushed to the driver, confirmed in one tap, and shown as _Confirmed_ on the board (FR1–FR8).

## Define your experiment parameters

- **Feature under test (from the M4 PRD):** B6 Driver Alerts only. B5 (step progress) and B1 (compliance checklist) are held out of both arms.
- **Persona (M2):** A fleet coordinator (dispatcher) at a mid-size 3PL, with the delivery driver as co-persona: a re-route only works if the driver receives and confirms it.
- **Expected outcome (from the M3 hypothesis):** Coordinators send re-routes from RouteLogic instead of re-sending them in WhatsApp, so more of them finish the daily workflow in-tool.
- **Primary success metric (M3):** % of coordinators completing the daily dispatch workflow in RouteLogic.
- **Baseline rate (M3 data):** 18% (Snapshot 2).
- **Guardrail metric & boundary:** Managers × Reporting CSAT ≥ 4.3. A drop of more than 0.2 from today's 4.5 means stop and investigate.
- **Minimum Detectable Effect (MDE):** +12 pp (18% → 30%), the 30% go/no-go floor set in M4.
- **Sample size per arm:** 198 coordinator-days per arm (two-proportion test, α 0.05 two-sided, 80% power). Unit = coordinator-day, e.g. ~10 coordinators per arm × 20 working days. This is an assumption, since the brief doesn't give a coordinator count for the pilot accounts.
- **Traffic split & test duration:** 50/50, randomized by dispatch team (depot) inside each of the 3 accounts, so a driver never sits between both arms. 4 weeks, covering 4 weekly cycles, the same as the pilot window.
- **Significance threshold:** p < 0.05, no deviation.

## Define your control and variant

- **Control (A), the current experience:**
  - The coordinator re-routes on the Live Dispatch Board.
  - There's no push to the driver: the change takes 8–15 min to arrive (BUG-2044).
  - So the coordinator re-sends it in the WhatsApp group or calls (UXR-02). Drivers drive from screenshots and paper manifests (UXR-06, UXR-12).
  - In the M3 workflow data:
    - Assign Routes takes 8.2 min vs. a 4.0 benchmark, and 29% never complete it in-tool.
    - Only 18% finish the daily workflow in RouteLogic.
- **Variant (B), one change: B6 Driver Alerts.**
  - Screens:
    1. **Board:** a re-route panel with "Send to driver".
    2. **Driver phone:** a lock-screen push "Route changed · New next stop: …", the updated route with the new stop highlighted, and a one-tap Confirm.
    3. **Board:** the badge goes Sent → Delivered → Confirmed with elapsed time, plus a "Not confirmed" flag after 2 min and Resend.
  - Functional requirements:
    - FR1: one push in ≤ 5 s.
    - FR2: the alert names the stop from the route record only.
    - FR3: the alert opens the route in 1 tap.
    - FR4: the driver confirms in 1 tap.
    - FR5: live status on the board.
    - FR6: every status change is logged with a timestamp (the measurement source).
    - FR7: the latest re-route replaces a pending one.
    - FR8: Cancel.
- **Isolation check, what has NOT changed:**
  - Same app version and release train for the coordinator web app and the driver app.
  - Same Live Dispatch Board, Route Optimizer and compliance logging: B1 is off in both arms.
  - B5 step progress is off in both arms. It was in the M4 pilot scope and is held out so B6 is the only change.
  - BUG-2072 (stale board status) is untouched in both arms.
  - Same onboarding and training: the CS lead runs the same session for both arms, and B6 gets only an in-product tooltip.
  - Same accounts, shift patterns and test weeks.
  - Same notifications apart from the B6 push. Manager reporting is unchanged.
  - Risk to watch: a control driver can't receive B6 alerts if their coordinator is in the variant arm. That's why we randomize by dispatch team, not by coordinator.

## Formalize your hypothesis & shipping criteria

- **Your hypothesis:** If coordinators can push a re-route straight to the driver and see it confirmed in one tap (B6), then their in-tool daily workflow completion will rise from 18% to at least 30%, because they no longer need WhatsApp to close the re-route loop. Managers × Reporting CSAT stays ≥ 4.3.
- **Your shipping criteria (judged at week 4, ~198 coordinator-days per arm):**
  - **Ship** (B6 to all pilot accounts, then GA with B1): B reaches ≥ 30% and beats A at p < 0.05, the guardrail holds (≥ 4.3), and the PRD evals pass (send → confirmed ≤ 30 s; 100% of unconfirmed re-routes flagged).
  - **Pivot** (keep B6, judge it with B1): B beats A significantly but stays below 30%. That points to compliance as the remaining break in the loop. The next test is B6 + B1 vs. B6.
  - **Kill or roll back:** no significant lift, or the guardrail falls below 4.3.
- **Hardest parameter to define, and did it change your hypothesis?** The MDE. The guide's "one change" rule made me split the M4 pilot. B6 tested alone can't touch the compliance step, which has the steepest drop-off. I kept 30% as the floor, so a likely honest result is "pivot". It didn't change the hypothesis. It changed _how much of it_ a single test can prove: B6 tests the re-route half of the loop, and B1 needs its own test.

## Findings & decision _(after running it)_

_Not run yet._
