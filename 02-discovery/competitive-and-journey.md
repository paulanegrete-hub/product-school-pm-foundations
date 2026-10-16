# Competitive Analysis & Journey Map

> **Module 2 · Lab 2 — ★ Deliverable 2.** Repo file `02-discovery/competitive-and-journey.md` — part of your submission.
> Do the lab in the **Module 2 · Exercise 2 Guide** (linked from the Module 2 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Competitive Analysis & Journey Map** slide of your Module 6 final deck. Builds on your `ai-synthesis.md` and your Module 1 `problem-hook.md`.

## Responses

- **Role, who are you solving for?:** A fleet dispatcher at a mid-size 3PL who assigns and re-routes drivers in real time across a shift.
  - **Co-persona: the delivery driver.** A re-route only works if the driver receives it and confirms it, and drivers carry most of the evidence (7 of 12 research notes: six interviews plus the focus group, UXR-01, 03, 05, 06, 08, 11, 12). Direct dispatcher evidence is thinner (UXR-02, UXR-09), so the dispatcher pain is a hypothesis to validate in Module 3.

- **Goal, what is this user ultimately trying to achieve?:** Seamless route orchestration: change a route once, know the driver has it right away, and trust that the board reflects what is happening on the road.

- **Friction, the main barrier (moment of misery) stopping them:** A reassignment takes 8–15 minutes to reach the driver, with no push notification, and the board shows "in progress" for stops delivered an hour ago. RouteLogic can't be trusted to run the live day, so the dispatcher leaves it.

- **External tools the user is forced to use:**
  - **WhatsApp group:** route changes and live coordination, "the real system" (UXR-02)
  - **Phone calls:** reading stops to drivers after a crash (UXR-03)
  - **Texts from drivers:** delivery confirmations instead of the 3-screen "mark delivered" (UXR-01)
  - **Driver-side backups the dispatcher depends on:** route screenshots (UXR-06) and paper manifests, kept by 5 of 7 focus-group drivers (UXR-12)

- **The process, the 3–5 manual steps they take:**
  1. Reassign the route in RouteLogic for the record, knowing it won't reach the driver for 8–15 min (BUG-2044).
  2. Send the same change in WhatsApp or call the driver so they actually turn around.
  3. Collect delivery confirmations by text, because "mark delivered" takes 3 taps across 3 screens (BUG-2055).
  4. Ignore the board and check status in chat, because it lags 20–60 min (BUG-2072).
  5. When the app crashes on a long route (BUG-2031), recover it by phone, with the office reading the stops aloud.

- **Core frustration, where the process feels most "broken":** The dispatcher does every change twice and still can't trust what RouteLogic says. Step 2, re-sending a change they already made, is where the product visibly loses the job to WhatsApp.
  - **Why it's inefficient:** double entry on every exception; no single, searchable source of truth; drivers keep driving the wrong way until the message lands; one crash costs ~20 min of a driver's and the office's time (UXR-03).
  - **Link to the business crisis:** if WhatsApp runs the day, a leaner competitor that "just does routing well" (UXR-04) only has to beat WhatsApp. The workaround drains daily adoption, which is now putting renewal at risk (UXR-10).

- **The evidence, a quote or behavior from the research:** "I reassign a route and the driver doesn't see it for ten, fifteen minutes. By then they've driven the wrong way. We keep a WhatsApp group as the real system." (UXR-02, fleet dispatcher, mid-size 3PL)

- **Journey map, a shareable link or the map file you committed:** [`journey-map.md`](journey-map.md) (current state + future state) · visual timeline: [`future-state-journey.html`](future-state-journey.html) · [shareable link](https://claude.ai/artifact/5jkoCH1ihGqq6xb7cCfYbZ)

## Competitive comparison

How the dispatcher can run a live re-route today. The research names the leaner competitor only by what it does, so its other cells are open questions, not assumptions.

| | RouteLogic today | WhatsApp workaround | Leaner competitor |
|---|---|---|---|
| **Re-route reaches the driver** | 8–15 min, no push (BUG-2044) | Instant, but manual and off the record | Unknown, to research |
| **Confirm a delivery** | 3 taps across 3 screens (BUG-2055) | Free-text message | Unknown, to research |
| **Trusted live status** | No, lags 20–60 min (BUG-2072) | Only in the dispatcher's head and chat | Unknown, to research |
| **Feeds admin reporting** | Yes, "genuinely powerful" (UXR-10) | No | Unknown, to research |
| **Ease for frontline users** | Low: users touch ~5% and can't find it (UXR-04) | High: everyone already uses it | "Just does routing well" (UXR-04) |

**Read:** WhatsApp wins on speed, RouteLogic wins on reporting. Velocity's opening is to match WhatsApp's speed without losing the record, before the competitor shows it can do both.
