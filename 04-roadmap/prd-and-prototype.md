# PRD & Prototype Sprint

> **Module 4 · Lab 2.** Repo file `04-roadmap/prd-and-prototype.md` — part of your submission.
> Do the lab in the **Module 4 · Exercise 2 Guide** (linked from the Module 4 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It deepens the top feature from your `roadmap-prd-prototype.md` and feeds the **Roadmap, PRD & Prototype** slide of your Module 6 deck.

## Responses

- **The "Now" feature I'm scoping (name + one-line core description):** B6 Driver Alert Notifications: a re-route reaches the driver's phone in seconds and is confirmed in one tap, so the coordinator stops re-sending it on WhatsApp. Full PRD: [`prd-b6-driver-alerts.md`](prd-b6-driver-alerts.md).
- **My finalized Must-Haves (after overriding the AI):** Push on re-route (≤ 5 s vs. 8–15 min today) · deep link to the updated route · one-tap confirm · Sent / Delivered / Confirmed status on the board · event logging of every status change. I promoted event logging from Should to Must: it doesn't touch the moment of misery directly, but without it the pilot can't be measured.
- **What I demoted from Must → Should/Won't, and why:** Compliance flag alerts, which are part of the B6 backlog description, moved to Won't (now). They depend on B1 (NEXT), and mixing them in would blur the one signal the pilot tests: does the re-route reach the driver? SMS fallback went to Could (V2): it needs an external provider, which 2 engineers can't absorb in 4 weeks.
- **One thing my PRD makes explicit that a vague brief would have missed:** What the alert is allowed to say. A vague brief says "notify the driver." My PRD says the alert text comes only from fields in the route record, nothing is generated, and a stop with missing data blocks the alert instead of sending a guess. In a moving vehicle, a wrong address is worse than a late one.
- **Where the prototype revealed a gap in my PRD logic (what I updated):** Two gaps. (1) Cancel only lived in Edge Cases, but building the board showed the coordinator needs a visible Cancel action on every pending re-route, so I added it as FR8. (2) The PRD didn't say what happens when a phone gets signal back after the 2-minute flag. The prototype delivers the alert on reconnect and keeps the flag until the driver confirms, and I added that rule to Smart Behaviors.
- **My shareable prototype URL:** [`04-roadmap/prototype-b6-driver-alerts.html`](prototype-b6-driver-alerts.html) (in this repo; opens in any browser).
