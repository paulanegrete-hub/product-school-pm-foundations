# Journey Map: The Fleet Dispatcher's Live Re-Route

**Persona:** Fleet dispatcher, mid-size 3PL (UXR-02, UXR-09)
**Scenario:** A delivery goes wrong mid-route and a stop has to be reassigned.
**Sources:** Module 2 user research (UXR-xx) and bug reports (BUG-xxxx). Emotions are inferred from the quotes; anything not in the research is marked *assumption*.

| Stage | 1. Exception hits | 2. Reassign | 3. Reach the driver | 4. Track the fleet | 5. Recover from failure |
|---|---|---|---|---|---|
| **Dispatcher action** | Learns a stop or route needs to change | Reassigns the route in RouteLogic | Re-sends the change in WhatsApp or calls the driver | Asks drivers in chat what is really done | Office reads remaining stops to the driver by phone |
| **Tool used** | RouteLogic + WhatsApp | RouteLogic | **WhatsApp / phone** | **WhatsApp / driver texts** | **Phone** |
| **What breaks** | — | Change takes 8–15 min to reach the driver, no push (BUG-2044) | Double entry on every change | Board shows "in progress" for stops delivered an hour ago (BUG-2072); confirmations arrive by text because "mark delivered" takes 3 screens (BUG-2055) | App crashes past ~40 stops and loses the route (BUG-2031) |
| **Evidence** | — | "The driver doesn't see it for ten, fifteen minutes" (UXR-02) | "We keep a WhatsApp group as the real system" (UXR-02) | "I can't trust the board" (UXR-09) | "Twenty minutes gone" (UXR-03) |
| **Emotion** *(inferred)* | Alert | Doubtful | Frustrated, doing it twice | Distrustful | Firefighting |

**Moment of misery:** Stage 3. The dispatcher has already done the job in RouteLogic, and still has to leave it to make the change real.

**Outcome:** The real state of the fleet lives in a chat thread. RouteLogic holds a lagging record, updated later if at all (*assumption from Module 1, not in the research*).

---

## Future State: Velocity (4 stages)

**Persona:** fleet dispatcher (primary) and delivery driver (co-persona).
**Strategy:** reclaim operational simplicity and make the core loop reliable: strip legacy noise, and make every change reach the driver in seconds.
**Visual timeline:** [`future-state-journey.html`](future-state-journey.html) · [shareable link](https://claude.ai/artifact/5jkoCH1ihGqq6xb7cCfYbZ)

1. **Spot the exception**
   - **User action:** Live board flags the late stop → spots it without asking in chat
   - **Internal state:** "I can see it. I don't have to ask."
   - **Pain point addressed:** Board lags 20–60 min (BUG-2072, UXR-09)
2. **Re-route in one move**
   - **User action:** Drags the stop to a nearby driver from home → no menus to dig through
   - **Internal state:** "That was one step."
   - **Pain point addressed:** Core actions buried 2–3 levels deep (BUG-2079, UXR-04, UXR-11)
3. **The driver gets it now**
   - **User action:** Change pushes to the driver, who taps accept → confirmed in seconds
   - **Internal state:** "Done once, and it landed."
   - **Pain point addressed:** 8–15 min lag, no push, WhatsApp re-send (BUG-2044, UXR-02)
4. **Trust the board**
   - **User action:** Driver closes the stop in one tap → board updates live
   - **User action:** Admin reporting sits one layer away → enterprise value kept, noise gone
   - **Internal state:** "The board is the truth. I can mute the WhatsApp group."
   - **Pain point addressed:** 3 screens to mark delivered, texted confirmations (BUG-2055, UXR-01, UXR-12)

**Competitive advantages over the manual workaround**
1. **One entry, not two:** a change made once reaches the driver; WhatsApp always needs a second send.
2. **One record everyone trusts:** live status replaces chat threads nobody can search, audit or hand over.
3. **It feeds what customers pay for:** taps land in the admin reporting that sold the product (UXR-10); texts never do.

**Dependency:** stripping noise fixes stages 2 and 4. Stage 3 needs the sync fix behind BUG-2044, which is why reliability is part of the strategy.

**Out of scope:** mid-route crashes (BUG-2031, Critical), offline mode (BUG-2050, High) and photo upload failures (BUG-2061, High). They hurt the driver, but they don't cause the re-route loop this initiative targets. Crash rate is tracked as a guardrail so Velocity doesn't make it worse.
