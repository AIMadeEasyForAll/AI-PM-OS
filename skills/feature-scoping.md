# Skill: Feature Scoping

Use this skill to turn a vague feature idea into a scoped, shareable definition that engineering can estimate and leadership can approve.

## When to use this

- A stakeholder hands you an idea with no shape ("can we add X").
- You need a written scope before a planning or estimation meeting.
- You're deciding whether something is an MVP slice or a larger initiative.

## Inputs needed

Paste in:
- The raw feature idea or request, in whoever's words it came in.
- Who asked for it (customer, exec, support, sales, data).
- Any existing constraints (deadline, team size, dependencies).

## Method

1. **Problem statement.** Write one sentence: who has what problem, and what's the cost of not solving it. If you can't write this sentence, the feature isn't ready to scope.
2. **User story.** `As a [user], I want [capability], so that [outcome].` One primary story. Secondary stories go in a list below it, not folded into the same sentence.
3. **Jobs-to-be-Done.** Separate the functional job (what the user is trying to get done), the emotional job (how they want to feel), and the social job (how they want to be perceived), if relevant. Most features only need the functional job stated explicitly.
4. **Success metrics.** 1-3 metrics, each with a number or threshold. No metric without a number — "increase engagement" is not a metric.
5. **Risks.** List technical, adoption, and business risks separately. A risk without a mitigation or an owner is a flag, not a plan.
6. **Assumptions.** Anything you're treating as true without evidence. State each as "We are assuming X" so it's falsifiable later.
7. **MVP scope.** The smallest version that tests the problem statement. Explicitly list what's deliberately excluded and why.

## Output

Produce a filled-in [`PRD-template.md`](../artifacts/PRD-template.md) using the sections above. Don't invent metrics or user counts — if the data isn't given, write `[NEEDS DATA]`.

## Common failure modes

- Scoping the solution before the problem is written down. Always write the problem statement first, even if the requester already proposed a solution.
- Treating "the requester wants it" as a success metric. The requester wanting it is the reason to scope it, not evidence it worked.
- MVP scope that's actually the full feature with a different name. If nothing was cut, it isn't an MVP.
