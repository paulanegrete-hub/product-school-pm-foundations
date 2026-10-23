# Problem Hook & Value Proposition: RouteLogic Velocity

> **Module 1 · ★ Deliverable 1.** Repo file `01-product-thinking/problem-hook.md` — part of your submission.
> Do the lab in the **Module 1 · Exercise 2 Guide** (linked from the Module 1 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Problem, Value & Hypothesis** slide of your Module 6 final deck. (Your Module 1 · Exercise 1 discovery map lands in `strategic-map.md`.)

## 1. Chosen scenario

**Path:** RouteLogic

## 2. The strategic crisis

_The big-picture business risk. If the company does nothing for 12 months, what happens to its market position?_

> RouteLogic will lose its largest enterprise account to a leaner competitor, and others will follow. The people who run daily operations will move to faster tools. RouteLogic will be left as an expensive back-office system that nobody uses in real time. We will no longer be "the fastest tool on the market," just the most complicated one.

## 3. The moment of misery

_The specific point where the product fails the user, forcing a manual workaround (Google, spreadsheets, group texts, a competitor)._

> When a delivery goes wrong mid-route, the dispatcher reassigns it in RouteLogic, but the driver doesn't see the change for 8–15 minutes and gets no notification. So the dispatcher sends it again in a WhatsApp group or calls the driver, and stops trusting the board. In one dispatcher's words: "We keep a WhatsApp group as the real system." Meanwhile, an enterprise account is evaluating a leaner competitor that "just does routing well."
>
> _Revised after Module 2 research (UXR-02, UXR-04, BUG-2044)._

## 4. Problem hook

_One urgent sentence fusing the business risk and the user pain, your pitch for why this is the most important thing to work on right now._

> We must stop our largest accounts from switching to leaner competitors by making a live re-route reach the driver in seconds, so dispatchers no longer run the day from a WhatsApp group.

## 5. Value proposition

_Who it's for, the new value, and why it's urgent to launch now._

> For **regional fleet dispatchers and the drivers they coordinate**, we will **deliver a focused Velocity workspace where a re-route reaches the driver in seconds and is confirmed in one tap, with the enterprise features kept one layer away rather than removed**, because **an enterprise account is already evaluating a leaner competitor and renewal is at risk now**.

## 6. Cold-read self-review

_Read your hook back as a skeptical stakeholder. If you don't feel the urgency, that's your data._

| Question | Your answer |
|---|---|
| Is the business risk high enough to justify a new initiative, a high-stakes threat, or a minor inconvenience? | High stakes. An enterprise account is evaluating a leaner competitor (UXR-04) and renewal is at risk (UXR-10). The bigger signal is that frontline users touch only about 5% of the product (UXR-04) and work around the rest, so the risk goes beyond one account. |
| Is the moment of misery a systemic problem or just an edge case? | Likely systemic: across interviews, users keep parallel systems (WhatsApp, texts, screenshots, paper manifests for 5 of 7 drivers). But direct dispatcher evidence is thin (2 of 12 interviews, one from a mid-size 3PL rather than an enterprise account), so I present it as a hypothesis to validate. |
| Does the value proposition actually remove the obstacle you identified, or is it a generic feature? | Yes, once it targets the real bottleneck. The value isn't fewer clicks, it's no longer needing the phone: the change reaches the driver in seconds (BUG-2044). That's the difference between a generic feature and real value. |

## 7. Finalized hypothesis _(complete in Module 3)_

> Based on dispatchers running the day from a WhatsApp group (UXR-02) and only 18% of coordinators finishing their daily workflow in RouteLogic, I believe that a focused Velocity workspace that closes the assignment loop (the re-route reaches the driver in seconds and compliance is logged in the same flow) will move coordinators back into RouteLogic and reduce complexity-driven churn, as measured by a 2× increase in in-tool workflow completion (18% → 36%). I will protect Manager Reporting CSAT (≥ 4.3) and make a go/no-go decision at week 8 (a 4-week pilot followed by 4 weeks of GA).

_Completed in Module 3; full reasoning in [`03-analytics/hypothesis-and-metrics.md`](../03-analytics/hypothesis-and-metrics.md)._

## Link to full artifact

_[link to your Problem Hook Builder export]_
