# Skill: Discovery

Use this skill before scoping anything — it's how you find out whether the problem is real before you write a single requirement.

## When to use this

- You have a hypothesis about a user problem but no evidence yet.
- You're about to commit a quarter to something and want to de-risk it first.
- Conflicting signals are coming in (support says X, sales says Y) and you need to reconcile them.

## Inputs needed

- The hypothesis or question you're investigating.
- Whatever existing signal you already have (tickets, interview notes, analytics, NPS comments).
- Who you have access to talk to (customers, internal users, support, sales).

## Method

1. **State the hypothesis as falsifiable.** "Users churn because onboarding is confusing" is falsifiable. "Onboarding could be better" is not.
2. **Pick the cheapest test first.** Order: existing data review → support/sales interviews → 5 user interviews → survey → prototype test → live experiment. Don't run an experiment to answer a question existing data already answers.
3. **Write the interview or analysis plan before running it.** 3-5 questions max for interviews, each one mapped to a specific thing you're trying to learn — not "tell me about your workflow" with no target.
4. **Capture evidence, not opinions.** Direct quotes and specific behaviors go in the findings. "Users seemed frustrated" is an opinion; "3 of 5 users abandoned the flow at step 2 without completing it" is evidence.
5. **Synthesize into a verdict.** Hypothesis confirmed, partially confirmed, or rejected — and what you'd do differently because of it. Discovery that doesn't change a decision wasn't worth running.

## Output

A short discovery brief: hypothesis, method used, evidence gathered, verdict, and the resulting decision (proceed to scoping / reframe the problem / kill it). Feed a "proceed" verdict into [`feature-scoping.md`](feature-scoping.md).

## Common failure modes

- Interviewing people who already agree with you (your biggest fan, your own team) and calling it validation.
- Running discovery after the roadmap slot is already committed — at that point it's theater, not discovery.
- Treating a single anecdote as a pattern. Look for the third independent confirmation before calling something a trend.
