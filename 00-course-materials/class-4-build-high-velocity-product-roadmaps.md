<!-- Source: https://app.productschool.com/courses/pmc/product-management-oct13-26-weeknights/materials/class-4 · scraped 2026-10-29 -->
<!-- anchors: heading-class-recording heading-slides heading-resources-templates heading-student-notes 1-how-to-build-a-strategic-roadmap 2-lab-1-build-a-dynamic-clickable-feature-roadmap 3-foundations-of-effective-scoping 4-from-requirements-to-a-functional-prototype 5-lab-2-prd-to-prototype-rapid-validation-loop key-takeaways deliverables heading-glossary -->

# Build High-Velocity Product Roadmaps — Class Materials

## Class Recording

2h 5m

[Embedded: Class Recording · 2h 5m](https://us02web.zoom.us/rec/play/FpRvrrkFG-0aT0YcNG82YdhQsC58SD34dgCq_VgOVD9P0nGN6P2rqP2fdzO2wt55PxdIQ7d2s6WuWjwj.wCo_frbF9zamaDkv)

## Slides

[Embedded: Slides](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Slides%20(Shareable).html)

## Resources & templates

Deepen what we covered and feed your final-project deliverables.

- [🗺️ Lab 1 Guide + Roadmap Builder — The full roadmap walkthrough, backlogs, scoring prompts, and the interactive Effort×Value → Now/Next/Later builder.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Exercise%201%20Guide.html)

- [🛠️ Lab 2 Guide + PRD Builder — MoSCoW + Simplified PRD prompts and the interactive PRD Builder that exports a build-ready blueprint.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Exercise%202%20Guide.html)

- [🕹️ Example Roadmap & Sample PRD — The high-velocity example roadmap and the PulseAI sample Simplified PRD for reference.](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Example%20Roadmap.html)

## Class notes

# Module 4 · Notes: Sequence the Roadmap: Now, Next, Later

> Shareable class notes. Pairs with the [slides](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Slides%20(Shareable).html), the two lab guides, and the Roadmap & PRD builders.

## 1 · How to build a strategic roadmap

A product roadmap is not a static feature list, in high-growth environments it's your primary **strategic communication tool**, the bridge between vision and execution.

**The What**: a roadmap is a *visual strategy* (where you're going, in what order), a *prioritized sequence* (every item earned its place), a *living document* (only as good as its last update), and an *outcome map* (the goal is solving problems, not shipping code).

**The Why**: it *forces alignment* (agree on direction, not just dates), *protects focus* (the data to say "no"), *manages change* (pivot without churning the team), and *drives impact* (shifts from "what are we shipping" to "what problem are we solving").

**Three steps to build one:**

1. **Ideate & Collect**: secure leadership buy-in early, gather design/eng inputs as a feasibility reality-check, centralize concepts in one doc.

2. **Prioritize & Sequence**: score every initiative on Impact vs. Effort, maintain a 70/20/10 balance, map dependencies and risks.

3. **Communicate & Manage**: review with Sales/Compliance, publish a single source of truth, iterate on a defined cadence.

**Tools:** dedicated SaaS (ProductBoard, Aha!, Airfocus, Roadmunk, ProductPlan), vibecoding tools (AI Studio, Lovable, Bolt), or generic productivity (Airtable, Sheets, Excel/PowerPoint).

### The Effort vs. Value matrix

Your reality filter for the backlog. **Value** = anticipated lift on your M3 success metric; **Effort** = total technical cost, sized with engineering. You are the **gatekeeper of engineering time**.

- **Quick Win** (high value, low effort) → build now; the backbone of your 70% core.

- **Major Project** (high value, high effort) → a big bet for 20% adjacent / 10% innovation; schedule it properly.

- **Fill-In** (low value, low effort) → only when capacity frees up.

- **Time Sinker** (low value, high effort) → identify and kill before it ever reaches the roadmap.

*Spotify example (goal: retention):* Search Optimization = Quick Win · Personalized Recommendations / Offline Listening = Major Projects · Lyrics Integration = Fill-In · Social API Expansion = Time Sinker.

## 2 · Lab 1: Build a dynamic, clickable feature roadmap

Score your scenario's backlog with **Effort vs. Value**, use an LLM for a baseline, then **override with your M2/M3 evidence**: your research-backed judgment beats the AI's generic scoring. Convert the finalized table into a clickable **Now / Next / Later** roadmap with a **Cut List** for the time-sinkers. → [Lab 1 Guide](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Exercise%201%20Guide.html) · [Roadmap Builder](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Roadmap%20Builder.html)

## 3 · Foundations of effective scoping

**MVP** = the most pared-down version that still delivers the core value. Two steps: **define the core value** (one high-value outcome) and **map the essential flow** (the shortest happy path). Focus on the experience, not the interface.

**MoSCoW** slices scope: **Must** (ship-blocker) · **Should** (high-priority-if-capacity) · **Could** (next-sprint polish) · **Won't (now)** (explicit exclusion). The kill test: *"if we remove this, can the user still achieve the primary outcome?"*

*Spotify Search example:* Core Keyword Matching = Must · Auto-Suggest = Should · Voice-to-Text = Could · Social Search = Won't (now).

## 4 · From requirements to a functional prototype

The build is moving from waterfall (write a huge doc, wait months) to a **rapid validation loop**: Discover (your hypothesis) → **Design** (Simplified PRD → AI prototype, iterate) → Deliver (experiment, then GTM).

**The PRD** centralizes the *why*, forces clarity (if you can't describe it in plain English, the AI will hallucinate the gaps), and bridges strategy to execution. It's never "finished", in the loop it *is* the functional prompt.

**Traditional vs. Simplified PRD:** the Simplified PRD swaps long scenarios and logistics for a **Vision**, a **Press Release**, **Smart Behaviors**, **Edge Cases**, and a light **Eval**: making it feedable straight into a prototyping tool. See the [sample PRD](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Sample%20PRD.html) (PulseAI) for a worked example.

**The alignment handshake:** shop the PRD *and* prototype together to the **Manager** (strategic green light), the **Eng Lead** (feasibility + simpler paths), and the **Design Lead** (UX polish). The PRD gives the rules; the prototype gives the feeling.

## 5 · Lab 2: PRD-to-Prototype rapid validation loop

Zoom into your top "Now" feature, scope it with **MoSCoW**, write a **Simplified PRD**, and feed it into your vibe-coding tool to generate a clickable prototype. A V1 is enough, focus on whether the core "moment of misery" solution functions. → [Lab 2 Guide](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20Exercise%202%20Guide.html) · [PRD Builder](https://app.productschool.com/lms/student/content/pmc%402026.1/outputs/certifications/pmc/2026.1/Modules/Module%204%20-%20PRD%20Builder.html)

## Key takeaways

1. **Roadmaps prioritize problems, not features**: aligned on continuous, validated value.

2. **Scoping prevents mission creep**: MoSCoW separates non-negotiables from enhancements to protect the timeline.

3. **The Simplified PRD is a functional blueprint**: it bridges strategy and execution to drive an automated build.

4. **Rapid prototyping de-risks before you commit eng**: turn theoretical requirements into clickable realities in minutes.

## Deliverables

- A **Now / Next / Later roadmap** (in your project repo).

- A **shareable, clickable prototype** link.

*Next module: Call the Test: Ship, Iterate, or Kill, A/B testing to ship, kill, or iterate.*

## Glossary

# Module 4 · Glossary: Sequence the Roadmap: Now, Next, Later

**Product roadmap**: A visual strategy that communicates where the product is going and in what order. Functions as a planning, communication, and negotiation tool at once: it forces alignment, protects focus, manages change, and drives impact.

**Now / Next / Later**: The three lanes of a high-velocity roadmap. *Now* = building this sprint (the MVP core); *Next* = the following 1 to 2 sprints (big bets); *Later* = backlog / spare capacity.

**Effort vs. Value matrix**: A 2×2 prioritization framework. **Value** = the anticipated lift on your success metric; **Effort** = the total technical cost. It produces four quadrants:

- **Quick Win** (high value, low effort) → *Now*. Your MVP core.

- **Major Project** (high value, high effort) → *Next*. A big bet to schedule properly.

- **Fill-In** (low value, low effort) → *Later*. Cheap, non-strategic; do in spare capacity.

- **Time Sinker** (low value, high effort) → *defer / kill*. Cut before it touches the roadmap.

**70 / 20 / 10**: A balanced split of roadmap capacity: ~70% core product, ~20% adjacent growth, ~10% exploratory innovation.

**ROI (Return on Investment)**: The value delivered relative to the engineering cost; the lens for protecting your most limited resource (engineering capacity).

**MVP (Minimum Viable Product)**: The most pared-down version of a solution that still delivers the core value proposition. Defined by two steps: *define the core value* (the single high-value outcome) and *map the essential flow* (the shortest "happy path" to it).

**Happy path**: The shortest, simplest sequence of steps a user takes to reach the core value, stripped of edge cases and polish.

**MoSCoW**: A scoping framework that sorts requirements into:

- **Must-Have**: a ship-blocker; required for the feature to function at all.

- **Should-Have**: high priority; valuable if capacity allows, otherwise V1.1.

- **Could-Have**: polish or enhancement; a next-sprint / V2 nice-to-have.

- **Won't-Have (now)**: an explicit exclusion that prevents scope creep.

**Scope creep**: The uncontrolled expansion of a build's requirements; MoSCoW and explicit Won't-Haves are the guardrails against it.

**PRD (Product Requirements Document)**: The central communication tool that aligns a team on the purpose, functionality, and success of a feature; a living blueprint guiding design and development.

**Traditional PRD**: The heavy "alignment doc" used to coordinate large cross-functional teams over months. Thorough but slow.

**Simplified PRD**: A lean "build doc" optimized for the rapid validation loop. Trades long scenarios and logistics for a **Vision**, a **Press Release**, **Smart Behaviors**, **Edge Cases**, and a light **Eval**: and doubles as a functional prompt for an AI prototyping tool.

**Press Release**: A short, punchy announcement format inside a Simplified PRD that defines user value in one or two paragraphs; also a great high-level prompt for an AI tool.

**Smart Behaviors**: The If/Then logic rules (Situation → Outcome) that tell an AI prototyping tool how the system should respond, preventing hallucinated behavior.

**Edge cases / Unhappy paths**: Non-ideal inputs and states (empty input, errors) the prototype must handle, including a **safety / hallucination guard** defining what the system must never do or invent.

**Eval (Light Eval)**: A short set of measurable targets (e.g., % accuracy, time-on-task, safety triggers) that define whether the AI's output is actually accurate and helpful.

**Rapid validation loop**: The high-velocity design cycle: prompt the tool → test the functional output → identify logic gaps → update the PRD → repeat, until the logic is bulletproof.

**Vibe coding**: Using AI prototyping tools (e.g., Lovable, Bolt, AI Studio) to generate functional, clickable prototypes from natural-language requirements.

**Builder hook**: A short executive instruction pasted above a PRD in a vibe-coding tool ("Build a working prototype based on this PRD…") that frames how the tool should interpret the document.

**Alignment handshake**: Shopping the PRD *and* prototype together to three stakeholders: the **Manager** (strategic green light), the **Eng Lead** (technical feasibility), and the **Design Lead** (UX polish). The PRD provides the rules; the prototype provides the feeling.
