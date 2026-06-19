# Skill: Metrics

Use this skill to define what "worked" means before you ship, not after — and to pick metrics that can actually be moved by the thing you're building.

## When to use this

- Scoping a feature and you've reached the "success metrics" step.
- A metric is being debated ("is this even the right thing to measure?").
- Reviewing whether something that shipped actually worked.

## Inputs needed

- The problem statement and user story this feature serves.
- What's already instrumented (don't propose a metric with no data source).
- The north star metric or business goal this should ladder up to.

## Method

1. **Separate leading and lagging indicators.** Lagging metrics (revenue, retention) confirm long-term success but move slowly and are influenced by many things. Leading metrics (adoption rate, time-to-first-value, task completion) move fast and are more directly attributable — use these for shipping decisions, lagging metrics for quarterly reviews.
2. **Pick one primary metric.** A feature with five "success metrics" has none — you can't act on a mixed signal. Pick one primary, and at most two guardrails (metrics that shouldn't get worse).
3. **Set the threshold before launch, not after.** "We'll know it worked if X" written before you see the data. Writing it after you see the number is rationalization, not measurement.
4. **Confirm instrumentation exists before committing to a metric.** If you can't currently measure it, that's a separate engineering task, not a footnote.
5. **Define the measurement window.** A metric with no time bound never resolves to a verdict — "increase adoption" needs "...by 15% within 6 weeks of launch."

## Output

A metrics block: primary metric (with threshold and window), guardrail metrics, data source for each, and the decision this measurement will drive (ship as-is / iterate / roll back).

## Common failure modes

- Choosing vanity metrics (page views, signups) over metrics tied to retained value (activation, repeat usage).
- Defining success after looking at the data ("well, a 3% lift is actually pretty good") instead of before.
- Picking a lagging metric as the primary signal for a fast-iterating feature — by the time it moves, you've shipped three more changes and lost attribution.
