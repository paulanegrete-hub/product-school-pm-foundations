# GTM Strategy & Success Dashboard (Module 6)

> **Module 6 · ★ Deliverable 6.** Repo file `06-launch/gtm-and-dashboard.md` — part of your submission.
> It becomes the **GTM Strategy & Success Dashboard** slide of your Module 6 final deck.

## Go-to-market summary

A **Tier M, engagement-led launch** of **B6 Driver Alerts** to existing customers, not a new market. The goal is behaviour change: coordinators stop re-sending re-routes in WhatsApp, and drivers turn on push and confirm in one tap. Three owned channels carry it: in-product prompts, CS-led depot onboarding, and an account email plus renewal review with ops managers. There's no paid spend. Beta in weeks 1–4 (the M5 A/B test at 3 pilot accounts), launch moment in week 5 with the GA start, go/no-go in week 8. Then the results go to the enterprise renewals at risk.

## Success dashboard

| KPI | Baseline | Target | Measurement window |
|---|---|---|---|
| In-tool daily workflow completion (primary) | 18% | ≥ 30% floor, 36% target | Week 8 |
| Pilot drivers with push alerts enabled | 0% (no push today) | ≥ 90% | End of week 1 |
| Send → confirmed time | 8–15 min, no push (BUG-2044) | ≤ 30 s | Weeks 1–4 |
| Unconfirmed re-routes flagged at 2 min | 0% (not tracked) | 100% | Weeks 1–4 |
| Managers × Reporting CSAT (guardrail) | 4.5 | ≥ 4.3 | Week 8 |

_Push opt-in is a precondition, not an outcome. Every driver without push falls back to WhatsApp, which dilutes the B6 arm. I set the 90% target myself (the brief gives no baseline), and I'd revisit it after week 1._

## Get your prior work ready

- **The feature you're launching (from the M4 PRD):** B6 Driver Alerts. A re-route is pushed to the driver in ≤ 5 s, confirmed in one tap, and shown as Sent → Delivered → Confirmed on the board.
- **What your M5 experiment told you:** The test hasn't run yet. This plan is built for the **Ship** result: B ≥ 30% completion, p < 0.05, guardrail ≥ 4.3, PRD evals pass. If the result is **pivot** (a real lift but below 30%), B6 stays on and the launch moment waits for B6 + B1.
- **Your persona (M2):** A fleet coordinator (dispatcher) at a mid-size 3PL, with the delivery driver as co-persona.

## Set your goal, then your audience

- **Primary GTM goal:** Engagement.
- **Why this goal?** It's a retention problem, not acquisition. These customers already pay, but their coordinators run the day from WhatsApp. Success means existing users send re-routes from RouteLogic and finish the day there (18% today).
- **Target audience:** Coordinators and their drivers at the 3 pilot accounts, then at the enterprise accounts at renewal risk (UXR-04, UXR-10). Ops managers are a secondary audience: they don't use B6 daily, but they sign the renewal.

## Size your launch

- **Launch tier:** M (targeted).
- **Justification:**
  - **Reach:** existing accounts only.
  - **Revenue impact:** it protects renewals instead of opening new revenue.
  - **What silence would risk:** if drivers never turn on push and coordinators never hear "you can stop re-sending in WhatsApp," the habit stays and the feature looks like it failed. That's why S isn't enough.
  - **Why not L/XL:** no new market, no new pricing.
- **Launch or release?** A launch. It asks two groups to change behaviour: coordinators drop WhatsApp, and drivers allow push and tap Confirm. Shipping it quietly wouldn't move the metric.

## Choose your top three channels and plan assets

- **Channel 1, owned: in-product.** A one-time prompt on the board ("Re-routes now reach the driver in seconds") and a push-permission ask in the driver app. It reaches both personas at the moment they re-route.
- **Channel 2, owned: CS-led depot onboarding.** A 15-minute session per dispatch team, plus a driver quick card. It changes a habit, which an email can't do, and the CS lead already runs pilot onboarding.
- **Channel 3, owned: account email + renewal review with ops managers.** It shares the pilot results (send → confirmed time, completion lift) and turns the feature into a reason to renew for the person who signs. No paid channel: the audience is already a customer.
- **Enablement & assets:**
  - **Coordinators:** one-pager "How a re-route works now".
  - **Drivers:** quick card covering turning on notifications, Confirm, and what the "Cancelled" alert means.
  - **Demo:** a 2-minute video recorded from the prototype.
  - **CS:** FAQ covering no signal, two changes in a row, and Cancel.
  - **Support:** reply template for "my driver didn't get the alert".
  - **Account team:** renewal slide with the pilot numbers.

## Make it executable

- **Ownership (one person each, named by role because the brief names no individuals):**
  - **PM (Paula Negrete):** launch plan, go/no-go, renewal slide.
  - **Designer:** in-product prompt, driver quick card, demo video.
  - **Engineer 1:** push delivery and status logging (FR6, the measurement source).
  - **Engineer 2:** release, plus a feature flag per dispatch team.
  - **CS lead:** depot sessions, FAQ, support reply template.
- **Budget & resource gaps:**
  - No paid spend.
  - The gap is people. One CS lead can't onboard every enterprise account after the pilot, so it only scales with B10 In-App Training (LATER backlog).
  - There's no marketing or sales-enablement owner, so the renewal slide falls to the PM.
- **Timeline:**
  - **Phase 1, beta:** weeks 1–4, the M5 A/B test at the 3 pilot accounts.
  - **Phase 2, launch moment:** week 5. B6 goes to every team in the pilot accounts, alongside the GA start with B1.
  - **Phase 3, post-launch:** weeks 5–8, ending in the go/no-go at week 8. Results then go to the at-risk renewals.

## Define how you'll know it worked

- **Success metrics:**
  1. In-tool daily workflow completion, 18% → 36% (floor 30%).
  2. Pilot drivers with push enabled, ≥ 90% by end of week 1.
  3. Send → confirmed ≤ 30 s.
  - Guardrail: Managers × Reporting CSAT ≥ 4.3.
- **Bad signal to watch for:** alerts are delivered and confirmed fast, but completion doesn't move and the WhatsApp group stays active. That means the re-route wasn't the only break in the loop.
- **Most likely post-launch decision:** Iterate. B6 lifts completion but stays below 30%, because the compliance step (71% → 48% drop-off) is untouched. Next step: ship B1 and judge B6 + B1 at week 8.
  - **Double down** if completion reaches ≥ 30% and the guardrail holds.
  - **Deprioritize** if there's no lift.
