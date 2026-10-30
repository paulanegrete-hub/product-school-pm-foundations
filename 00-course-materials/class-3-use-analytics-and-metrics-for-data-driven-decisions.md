<!-- Source: https://app.productschool.com/courses/pmc/product-management-oct13-26-weeknights/materials/class-3 · scraped 2026-10-29 -->
<!-- anchors: heading-class-recording heading-slides heading-resources-templates heading-student-notes the-big-idea 1-how-metrics-define-success 2-methods-to-quantify-user-friction 3-the-data-to-hypothesis-flow key-takeaways your-deliverable heading-glossary -->

# Use Analytics and Metrics for Data-Driven Decisions — Class Materials

## Class Recording

2h 10m

[Embedded: Class Recording · 2h 10m](https://us02web.zoom.us/rec/play/DHpY-IRYzGT3RXdqacvcrsF7WmNj01r_GjJOWx5vQqxDiwgApQK4z_h4j1pRRb_c-iMuN2AaUR-4ncHq.5HZe3ZrJxn8jqp3G)

## Slides

[Embedded: Slides](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Slides%20(Shareable).html)

## Resources & templates

Deepen what we covered and feed your final-project deliverables.

- [🧭 Exercise Guide — The full hypothesis walkthrough, pre-work table, both scenarios' data snapshots, reflections, and the hypothesis template.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Exercise%20Guide.html)

- [🧪 Hypothesis Builder — Interactive worksheet to reconcile your evidence and draft a data-backed hypothesis, export to markdown.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Hypothesis%20Builder.html)

- [📖 Pre-Read — A 10-minute primer to arrive ready: vanity vs. strategic metrics, AARRR, and the hypothesis formula.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Pre-Read.html)

## Class notes

# Module 3 · Notes: Turn a Metric Into a Testable Hypothesis

> Shareable notes covering everything from the Module 3 session. Pair with the [slides](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Slides%20(Shareable).html), the [Exercise Guide](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Exercise%20Guide.html), the [Hypothesis Builder](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Hypothesis%20Builder.html), and the [reference card](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Metrics%20%26%20Hypothesis%20Reference%20Card.md).

## The big idea

Data is cheap; the *right metric* is expensive. Your job isn't to read dashboards, it's to find the one signal that proves a user's life actually got better (not just that they clicked your new button), locate *where* the friction lives, *size* how urgent it is, and turn it all into a measurable bet.

The flow for the day: **Define success → quantify friction → write the hypothesis.**

## 1 · How metrics define success

### Vanity vs. strategic (the success-metric showdown)

A savings app launches "Instant Transfer." Which is the better signal?

| | Metric | Verdict |
| --- | --- | --- |
| **A** | Total dollars moved via Instant Transfer | ❌ Vanity, measures the *action*, not value. Money can flow in today and out tomorrow. |
| **B** | % of users holding a higher balance 30 days after their first transfer | ✅ Strategic, a time-bound threshold proves the user actually saved. |

> Find the metric that proves the user's life improved, not just that they used your feature.

### The 3 pillars (and 3 traps)

- **Clarify the goal**: usage (initiative) or value (success)?

- **Focus on control**: can your build move it? (Avoid "Total Revenue.")

- **Maintain balance**: watch a **counter-metric** so a win doesn't break another area.

Traps: **False Signals** (vanity clicks) · **Lack of Context** (the *why* is in your research) · **Averages** (hide segment friction).

> **Leading vs. lagging:** for a language app's Quick-Start, 7-day retention is a *lagging result*, by the time it drops, the user is gone. Track the *leading indicator* you control: % completing the first lesson.

### The AARRR funnel

| Stage | Goal | Metric |
| --- | --- | --- |
| Acquisition | Get users in the door | Signup rate |
| **Activation** ⭐ | Deliver the "Aha!" | Key action · time to first key action |
| **Retention** ⭐ | Build a lasting habit | % returning DAUs / MAUs |
| Revenue | Convert value to sustainability | LTV |
| Referral | Low-cost growth engine | NPS |

⭐ Activation and Retention are the stages a product build most directly controls.

### The outcome hierarchy (YouTube)

You don't "increase total revenue" on day one, you move levers within distinct journeys. Each persona has its own signals:

| | Consumers (Viewers) | Creators | Advertisers |
| --- | --- | --- | --- |
| Activation | 1st like/comment (Day 1) | 1st upload / monetization | 1st campaign (Wk 1) |
| Retention | DAU/MAU, return rate | Upload consistency, net subs | Repeat campaign spend |
| Revenue | Premium subs, Super Chat | RPM, total payouts | Ad spend (total) |

> Ad spend grows only if advertisers repeat → only if creators keep uploading → only if viewers keep watching. Know **which funnel you own.**

## 2 · Methods to quantify user friction

### Slice it: segmentation

A metric tells you *what*; segmentation tells you *where*. Four lenses:

| Lens | Question | Example |
| --- | --- | --- |
| Behavioral | One action but skip the next? | Instagram, friction was the **camera**, not the feed |
| Tenure | Day 1 or Day 30? | Duolingo, the leak was the first **180 seconds** |
| Environmental | Platform / device / region? | Airbnb, **Android** parity, not search |
| Account tier | Everyone or one tier? | Zoom, the 40-min limit hit **Free** users |

> Don't build for the average. Target the group where the gap is widest.

**Reading a dashboard:** top-row results (Revenue, LTV up) are just *result signals*. The move hides in the slices, e.g. High-Value = 43% of revenue (protect it), Cart Abandoners = a *product* failure (fix checkout), One-Time buyers = your highest-leverage LTV move (build a second-purchase journey).

### Size it: cohort analysis

A cohort = users who started at the same time. Tracking them separately *sizes* the problem:

- **Decline** (newer cohorts drop faster) = a **leak** → needs a *fix*.

- **Flatline** (everyone stops at the same point) = a **ceiling** → needs an *improvement*.

**Heatmap:** read **→** for one cohort's lifetime; read **↓** to compare cohorts at the same age. The W0→1 drop is usually the most controllable lever, and don't scale a leaky bucket (any cohort trending to 0% means acquisition spend is wasted).

### AI as your data analyst

| Task | Export | Ask |
| --- | --- | --- |
| Slice | User data by trait (CRM) | "Which segments underperform? Surprising differences?" |
| Size | 2+ cohort tables | "Compare [A] vs [B]. What shifted? Why?" |
| Audit | Feature-usage % by segment | "Least-adopted but strategic features, promote, redesign, sunset?" |

> AI gives patterns; you interpret what matters.

### Two diagnostic cases

- **Spotify DAU −37%** (cliff on Day 18): don't act on the aggregate, *slice* by device OS, check if the "active session" definition changed, isolate by region. Your gut gives a *why*; the business needs the *how much*.

- **Amazon checkout −72%** (Payment → Confirmation): slice by payment method/geo/device to size impact; check server logs (errors) vs. analytics pipeline (missing pings). In a code-red, reverting to a known-good state often beats patching under pressure.

## 3 · The data-to-hypothesis flow

### The decision formula

> Based on **[discovery evidence]**, we believe that **[solving problem X]** for **[persona]** will result in **[strategic outcome]**, as measured by a **[% change]** in **[success metric]**: protecting **[guardrail metric]**, deciding after **[decision window]**.

| Component | Worked example |
| --- | --- |
| Discovery evidence | 60% of new users abandon setup at the integration step |
| Persona | Non-technical founders |
| Problem | Simplify the API integration experience |
| Strategic outcome | Reduced setup friction |
| Success metric | 25% increase in 7-day onboarding completion |
| Guardrail | Integration error rate must not increase |

> Lead with the hypothesis, not "I want to build a tool." It shifts the conversation from *what* to *why it matters*.

### Where's your bet?

- **Optimizing the existing** → chase Retention / Conversion (plug a leak). *(Slack channel folders.)*

- **Exploring the blue sky** → chase Activation / user success (prove new value). *(Early Netflix DVD-by-mail.)*

Deciding early prevents measuring a blue-sky idea with optimization expectations.

### Audit: 4 common pitfalls

| Trap | Fix |
| --- | --- |
| Vague / broad | Name the [persona], [behavior], [success metric] |
| Biased framing | Frame around the [user problem], not your solution |
| Not testable | Tie to [discovery evidence] + a specific [% change] |
| Misaligned | Ask: "If validated, does it move the North Star?" |

## Key takeaways

1. **AARRR is your prioritization filter**: it separates vanity numbers from the leaks driving a crisis.

2. **Slice, then size**: segmentation finds *where*; cohort analysis sizes *how urgent*.

3. **A hypothesis is a measurable contract**: qualitative insight + quantitative evidence + a guardrail + a decision window.

4. **The reflection beats the spreadsheet**: AI surfaces patterns; your value is interpreting them and being willing to pivot.

## Your deliverable

A formal, data-backed hypothesis in your project repo. Build it in the [Hypothesis Builder](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Hypothesis%20Builder.html); work the data in the [Exercise Guide](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%203%20-%20Exercise%20Guide.html).

## Glossary

# Module 3 · Glossary: Turn a Metric Into a Testable Hypothesis

Quick definitions for the terms used in the deck, labs, and reference card.

**Vanity metric (false signal)**: A number that *feels* like success but measures an action rather than an outcome (e.g. total dollars moved, total clicks). Users can perform the action without getting any value.

**Strategic metric (product signal)**: A number that proves the user actually achieved the goal, usually with a time-bound threshold (e.g. *% of users who hold a higher balance 30 days after their first transfer*).

**Leading indicator**: An early signal your product build can directly influence (e.g. *% completing the first lesson*). Where you actually have control.

**Lagging result**: An outcome you can only observe after the fact (e.g. 7-day retention). By the time it drops, the user is already gone.

**Counter-metric (balance)**: A metric you watch to ensure a win in one area isn't breaking another (e.g. signups jump, but are those users retaining?).

**Initiative signal**: A metric that proves your specific feature is being *used* (crossing the threshold from stranger to active user).

**Product signal**: A metric that proves users are getting *value* and forming a habit (typically Retention).

**Result signal**: A high-level business outcome (Revenue, LTV) that aggregates many upstream initiatives.

**AARRR**: The lifecycle funnel: **A**cquisition (signup rate), **A**ctivation (key action / time-to-first-key-action), **R**etention (% returning DAUs/MAUs), **R**evenue (LTV), **R**eferral (NPS). Activation and Retention are the product "sweet spots."

**Outcome hierarchy**: Mapping each user segment's Activation → Retention → Revenue signals so every metric connects to the question "Are we creating meaningful value?"

**Segmentation (slicing)**: Breaking a metric down by a trait to find *where* the friction is. Four lenses: **behavioral patterns**, **user tenure**, **environmental factors** (platform/device/region), and **account tier**.

**The average trap**: Relying on a single aggregate number that hides segment-level friction (a feature can delight power users while failing beginners).

**Cohort**: A group of users who started using the product at the same time.

**Cohort analysis (sizing)**: Tracking cohorts separately over their lifetime to *size* a problem's urgency.

**Decline (leak)**: Newer cohorts dropping faster than older ones, a regression. Needs a *fix* to restore lost value.

**Flatline (ceiling)**: Every cohort stopping at the same point, stable but stagnant. Needs an *improvement* to break through.

**Cohort heatmap**: A grid of retention by cohort (rows) and age (columns). Read horizontally for one cohort's lifetime; read vertically to compare cohorts at the same age.

**Hypothesis (data-backed)**: A measurable bet that merges qualitative insight with quantitative evidence. Formula: *Based on [discovery evidence], we believe that [solving problem X] for [persona] will result in [strategic outcome], as measured by a [% change] in [success metric].*

**Success metric**: The leading indicator that tells you the gap is closing.

**Guardrail metric**: The metric that must *not* drop; it protects your existing base while you pursue the win.

**Decision window**: How much time or data you need before deciding to scale, pivot, or kill.

**Optimizing the existing**: Improving a known workflow or fixing identified friction; you typically chase Retention or Conversion (plugging a leak).

**Exploring the blue sky**: Validating a new-to-market idea or unmet need; you typically chase Activation and user success (proving new value exists).

**Pivot check**: The discipline of changing your bet when the data contradicts your gut, moving from a feeling to a data-backed decision.
