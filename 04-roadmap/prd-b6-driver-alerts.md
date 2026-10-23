# PRD · B6 Driver Alert Notifications

**Author:** Paula Negrete · **Status:** Draft · **Target:** High-Fidelity Prototype
_RouteLogic Velocity · Team: 2 engineers, 1 designer, 1 CS lead · 4-week pilot, 3 accounts_

## 1. The Big Picture

**Vision:** A re-route reaches the driver in seconds and is confirmed in one tap, so the coordinator never has to send it again on WhatsApp.

**Press Release**

> _RouteLogic Velocity closes the loop between dispatcher and driver._ Today, when a fleet coordinator at a mid-size 3PL reassigns a route, the driver doesn't see it for 8 to 15 minutes. By then they've driven the wrong way. Coordinators cope by re-sending every change in a WhatsApp group they call "the real system" (UXR-02), and they collect confirmations by text (UXR-01).
>
> With Driver Alert Notifications, every re-route sent from the Live Dispatch Board, which 91% of coordinators already use daily, becomes a push alert on the driver's phone. One tap opens the new route, a second tap confirms it, and the board shows the coordinator _Sent → Delivered → Confirmed_ in real time. Coordinators stop running a second system. Drivers stop driving from screenshots.

**Success Metrics**

- **Primary:** in-tool daily workflow completion among pilot coordinators, 18% → 36%.
- **Guardrail:** Managers × Reporting CSAT ≥ 4.3 (today 4.5).

**Decision window**

| Phase | Weeks | What we measure | Decision |
|---|---|---|---|
| Pilot (B6 + B5, 3 accounts) | 1–4 | The re-route reaches the driver and is confirmed in-app (see Evals: send → confirmed ≤ 30 s, 100% of unconfirmed re-routes flagged) | Move to GA with B1? |
| GA (B1 + B4) | 5–8 | Completion 18% → 36%, with a 30% threshold; guardrail ≥ 4.3 | Scale if ≥ 30% and the guardrail holds · pivot if it improves but stays below 30% · kill or roll back if the guardrail breaks |

Completion is judged at week 8, not week 4: the pilot only fixes the re-route half of the loop, and the compliance step (steepest drop-off, 71% → 48%) changes only when B1 ships.

## 2. The Details

### User Stories

1. **As a** fleet coordinator, **I want** a re-route to reach the driver's phone the moment I save it, **so that** I don't have to re-send it on WhatsApp.
   - AC: saving a re-route sends one push to the assigned driver, with no extra step.
   - AC: the board row moves to _Sent_ immediately.
2. **As a** delivery driver, **I want** to open and confirm the new route in one tap, **so that** I'm not driving from a screenshot or a text.
   - AC: tapping the alert opens the updated route, with the new next stop visible.
   - AC: a single "Confirm" button sets the status to _Confirmed_.
3. **As a** fleet coordinator, **I want** to see which drivers have confirmed, **so that** I only follow up with those who haven't.
   - AC: each re-route shows _Sent / Delivered / Confirmed_ with a timestamp.
   - AC: unconfirmed re-routes are flagged after 2 min.

### Screens to Build (3)

1. **Entry point: Live Dispatch Board (coordinator)**
   - List of active drivers with route, next stop and status.
   - "Re-route" action on each row.
   - Re-route panel: driver, current stop, new stop selector, "Send to driver" button.
2. **Feature core: Driver alert + route view (driver phone mock)**
   - Lock-screen push showing "Route changed · New next stop: …".
   - Updated route view with the new next stop highlighted and the old one struck through.
   - A large one-tap "Confirm" button.
3. **Success / confirmation: board status (coordinator)**
   - Row badge moving from _Sent_ to _Delivered_ to _Confirmed_, with timestamps.
   - Elapsed time from send to confirm (e.g., "Confirmed in 0:24").
   - "Not confirmed" flag and "Resend" button for stalled re-routes.

### Functional Requirements (from MUST HAVE)

| # | Rule |
|---|---|
| FR1 | Saving a re-route triggers exactly one push to the assigned driver within ≤ 5 s (vs. 8–15 min today, BUG-2044). |
| FR2 | The alert names the new next stop, taken only from the route record. |
| FR3 | Tapping the alert opens the updated route in ≤ 1 tap. |
| FR4 | The driver confirms with exactly 1 tap; there is no form and no free text. |
| FR5 | The board shows _Sent / Delivered / Confirmed_ per re-route, and it updates without a refresh. |
| FR6 | Each status change is logged with a timestamp (sent, delivered, confirmed). This is the pilot's measurement source _(override: S4 → Must)_. |
| FR7 | A second re-route to the same driver replaces the pending one; the driver never sees two conflicting routes. |
| FR8 | Every pending re-route has a Cancel action on the board; cancelling sends the driver "Route change cancelled" and voids the earlier alert. _(added after the prototype)_ |

### Smart Behaviors

| Situation | Outcome |
|---|---|
| Re-route saved | Push sent; row → _Sent_ |
| Driver's device receives the push | Row → _Delivered_ |
| Driver taps "Confirm" | Row → _Confirmed_ + elapsed time shown |
| No confirmation after 2 min | Row flagged "Not confirmed"; "Resend" button appears |
| New re-route while one is pending | The pending alert is replaced, and the driver sees only the latest route |
| Driver opens an outdated alert | Shows "This route was updated" and opens the latest version |
| Re-route has no assigned driver | "Send" is disabled with the hint "Assign a driver first" |
| Phone gets signal back after the 2-min flag | The alert is delivered on reconnect; the flag stays until the driver confirms _(added after the prototype)_ |

### Technical Constraints (what not to build in the prototype)

- No external APIs: the push, the delivery and the timing are simulated in-page.
- No login: the coordinator view and the driver view sit side by side on one screen.
- State with `useState` only: no backend, no database, no localStorage.
- Mock data: 5 to 6 drivers and routes, hard-coded.
- No maps SDK: stops are shown as a list.

## 3. The Logistics

### Features Out (WON'T HAVE now)

- **Compliance flag alerts:** they depend on B1 (NEXT).
- **Fix for stale board status (BUG-2072):** a separate bug, outside B6.
- **Manager / exec notifications:** not the persona, and they touch Reporting (guardrail).
- **WhatsApp integration:** the goal is to replace WhatsApp, not connect to it.
- **End-customer notifications.**
- **AI ETA inside the alert:** B7 is on the cut list.

### Edge Cases

- **Driver offline / push off:** the row stays on _Sent_ and is flagged after 2 min, and the coordinator follows up by phone. SMS fallback is V2.
- **Conflicting re-routes:** the latest one wins (FR7), and the earlier alert is invalidated.
- **Driver confirms an outdated route:** the confirmation is rejected and the latest route is shown.
- **Re-route to the wrong driver:** the coordinator cancels before confirmation (FR8), and the driver sees "Route change cancelled".
- **Safety / hallucination guard:** the alert text is built only from fields in the route record (driver, stop name, address). Nothing is generated or inferred. If the stop is missing from the record, the alert is blocked and the coordinator sees "Stop data missing". The confirm button is large and single-tap, so drivers can confirm without reading long text while driving.

### Decision Log

1. **Compliance flags out of B6.** The backlog description includes them, but they depend on B1, which is too big for the pilot. Mixing them in would also blur the one signal we're testing: does the re-route reach the driver?
2. **No SMS fallback in the pilot.** It would mean an external provider and a second message flow for 2 engineers in 4 weeks. Unconfirmed re-routes get flagged instead, and the coordinator follows up by phone.

### Evals

| Eval | Target |
|---|---|
| Accuracy: the alert's stop matches the route record | 100% of alerts |
| Time-on-task: from coordinator "Send" to _Confirmed_ on the board | ≤ 30 s in the prototype (vs. 8–15 min today) |
| Safety trigger: unconfirmed re-routes get flagged | 100% flagged at 2 min; 0 alerts sent with missing stop data |

## Appendix · MoSCoW

- **Must:** push on re-route · deep link to the updated route · one-tap confirm · confirmation status on the board · event logging _(promoted from Should)_
- **Should:** "Not confirmed" flag after 2 min · change summary in the alert · manual resend
- **Could (V2):** SMS fallback · voice readout / hands-free confirm · batching of changes · confirmation-time trends
- **Won't (now):** compliance flag alerts · BUG-2072 fix · manager notifications · WhatsApp integration · end-customer notifications · AI ETA in the alert
