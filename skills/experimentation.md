# Skill: Experimentation

Use this skill when you need a real test of a hypothesis — an A/B test, a phased rollout, or a controlled pilot — rather than a ship-and-hope.

## When to use this

- Two or more plausible solutions exist and you don't have conviction on which wins.
- A change is risky enough (revenue, retention, trust) that you want evidence before a full rollout.
- Leadership is asking "how do we know this worked" and "we shipped it" isn't a satisfying answer.

## Inputs needed

- The hypothesis, in the form: "If we [change], then [metric] will [move by X], because [mechanism]."
- The metric and threshold from [`metrics.md`](metrics.md).
- Available traffic/users for the test, and how long you can reasonably wait for significance.

## Method

1. **Write the hypothesis with a mechanism**, not just an outcome. "If we shorten the form, completion rate increases because friction drops" is testable and falsifiable. "If we shorten the form, things will be better" is not.
2. **Decide the test design before launch:** A/B split, phased rollout, or holdout. A/B needs enough volume for statistical significance — calculate the required sample size before committing to a duration, don't just pick "two weeks" by habit.
3. **Pre-register the success threshold and the minimum detectable effect.** If the result lands ambiguously, you already agreed what counts as a win before you saw the data.
4. **Define the guardrails.** What metric, if it drops, kills the test early regardless of the primary metric's performance.
5. **Decide the rollback plan before launch.** What "kill it" looks like operationally — feature flag, config change, code revert — should be known before you need it, not figured out under pressure.
6. **Read results against the pre-registered threshold, not against what would make the best story.**

## Output

An experiment brief: hypothesis with mechanism, design (A/B / phased / holdout), sample size and duration, primary metric and threshold, guardrails, rollback plan, and the resulting decision once data is in (ship to 100% / iterate / kill).

## Common failure modes

- Peeking at results early and stopping the test the moment it looks favorable — this inflates false positives significantly.
- No guardrail metric, so a test that tanks support tickets or trust runs to completion anyway.
- Treating a flat or negative result as a failure of the team rather than a valid, useful answer. A killed hypothesis that saved a quarter of wasted build time is a win.
