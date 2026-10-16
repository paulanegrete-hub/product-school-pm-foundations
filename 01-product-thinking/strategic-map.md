# Strategic Discovery Map

> **Module 1 · Lab 1.** Repo file `01-product-thinking/strategic-map.md` — part of your submission.
> Do the lab in the **Module 1 · Exercise 1 Guide** (linked from the Module 1 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It's the discovery groundwork behind your `problem-hook.md`.

**Exercise:** the same water-tracking app mapped three times, with a more specific prompt each round. Visual: [`prompt-to-mindmap.html`](prompt-to-mindmap.html).

| Round | Prompt | What came back |
|---|---|---|
| Step 1 · Baseline | "Create a mindmap for a water tracking app." | 10 branches, ~45 items, 5 user segments, no priority |
| V2 · Role + structure | PM role; features, user needs, potential problems | Same catalog, regrouped into 3 buckets |
| V3 · PM framing | Persona (busy adults 25–40 who forget), JTBD, friction, effort vs. impact, monetization trade-offs, retention risks, flag tensions | 5 ranked branches + 5 strategic tensions to debate |

## Responses

- **Feature with no strategic answer (why is this a 12-week priority?):** **Smart-bottle integration.** It shows up in the baseline twice (Integrations and Business model) but nothing explains why it matters in the next 12 weeks. Once V3 ranked it on effort vs. impact, it became a money pit: expensive hardware work, and few users own a smart bottle.

- **Feature that looks "correct" but has zero strategic weight:** **Streaks and badges.** Every tracker has them, so they look like table stakes. V3 shows the problem: motivation fades by week 3, and a broken streak is a reason to quit. They are cheap to build but don't solve the core job ("remind me at the right moment"). V3 rates them a fill-in.

- **V3 vs your Step 1 baseline — what changed, and was it your PM knowledge that forced usefulness?:**
  - **Baseline:** a feature catalog for everyone (office workers, athletes, pregnant users, older adults). Complete, but nothing to decide.
  - **V2:** adding the PM role changed how it was organized, not what it said. No persona, no trade-offs.
  - **V3:** one persona with one failure mode ("they know, but they forget"). That turned features into a ranked bet: widget + watch one-tap logging and a simple personal goal are quick wins; calendar-aware reminders are the big bet.
  - **Yes, PM knowledge forced the usefulness.** The AI never prioritized on its own. Each useful output came from a framework I asked for: JTBD, effort vs. impact, monetization trade-offs, and "flag the tensions."
  - **Most valuable output:** the tensions. "Is the problem *logging is hard* or *I forget to drink*?" decides the build, and that question only appeared once the persona was narrow.
