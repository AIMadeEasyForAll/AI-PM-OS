# Skill: Prioritization

Use this skill to decide what to build next when you have more validated ideas than capacity — which is most of the time.

## When to use this

- Planning the next sprint, quarter, or roadmap pass.
- A stakeholder is pushing their item to the top and you need a defensible, repeatable answer for why it is or isn't.
- You have a backlog that's grown faster than anyone has triaged it.

## Inputs needed

- The list of candidate items (already scoped, or at least roughly understood).
- Whatever effort estimate exists for each (even rough: S/M/L/XL).
- The current top-level business goal or north star metric this prioritization should serve.

## Method

1. **Filter to one goal at a time.** Prioritize against a single goal (e.g. "reduce activation drop-off"), not a blended average of every goal at once — blended scoring hides the real tradeoff.
2. **Score each item on reach, impact, and confidence**, separately from effort:
   - Reach: how many users/accounts this touches in a defined time window.
   - Impact: how much it moves the target metric, on a 0.25/0.5/1/2/3 scale (minimal/low/medium/high/massive).
   - Confidence: how sure you are about reach and impact — high/medium/low, as a percentage multiplier (100/80/50%).
3. **Divide by effort** to get a relative score. This is RICE; use it as a forcing function for discussion, not as an oracle — a score of 41 vs 38 is not a meaningful difference.
4. **Sense-check against strategy.** An item can score well and still be wrong if it doesn't fit where the product is going. State explicitly if you're overriding the score and why.
5. **Write the cut line.** Don't just rank — say where the line falls given current capacity, and what falls below it.

## Output

A ranked list with: item, reach, impact, confidence, effort, score, and a one-line rationale for anything moved up or down off-score. Make the cut line visible.

## Common failure modes

- Scoring effort using whoever's most optimistic estimate. Use the engineer's number, not the requester's.
- Re-running prioritization every time someone complains, instead of on a fixed cadence — this trains stakeholders to escalate rather than to use the process.
- Treating "the loudest stakeholder" as a proxy for reach or impact.
