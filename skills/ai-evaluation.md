# Skill: AI Evaluation

Use this skill when the feature you're scoping or shipping involves a model — an LLM, a retrieval system, a classifier — and "it feels right" isn't a defensible definition of done.

## When to use this

- Scoping any feature where an LLM or ML model produces user-facing output (RAG, summarization, classification, agents).
- Deciding whether a model change (prompt update, model swap, new retrieval source) is safe to ship.
- A stakeholder asks "how do we know the AI is working" and you need more than a demo to answer.

## Inputs needed

- What the model is supposed to do, in the same problem-statement form as [`feature-scoping.md`](feature-scoping.md).
- Example inputs and what a good vs. bad output looks like for each — at least 10-20 real or representative examples.
- Any existing eval harness, logging, or human review process already in place.

## Method

1. **Define what "good" means before you have a model to judge.** Write 3-5 criteria a human reviewer could apply consistently (e.g. factual accuracy against source documents, refusal on out-of-scope questions, response length, tone). Vague criteria like "helpful" produce inconsistent ratings.
2. **Build a test set, not a demo set.** Include the easy cases, the edge cases, and the cases you expect to fail. A test set with only easy cases tells you the model can do the easy thing — already assumed.
3. **Decide the scoring method:** rubric-based human review for nuanced criteria (tone, helpfulness), exact-match or rule-based checks for deterministic criteria (does it cite a source, does it stay under N words), and LLM-as-judge only for criteria you've validated correlate with human judgment.
4. **Set a release threshold before evaluating**, same as [`experimentation.md`](experimentation.md) — e.g. "ship if ≥85% of test cases score 'acceptable' or above, and zero cases score 'harmful.'"
5. **Re-run the same test set on every material change** (prompt, model version, retrieval source) so you can tell regression from noise.
6. **Track failure modes, not just a pass rate.** A 90% pass rate where the 10% failures are all the same root cause is a different problem than 10% scattered failures.

## Output

An eval plan: success criteria, test set description (size, source, edge case coverage), scoring method per criterion, release threshold, and the regression process for future changes. Pairs with [`evaluation-template.md`](../artifacts/evaluation-template.md).

## Common failure modes

- Evaluating only on cases the model already handles well, because that's what's in the demo.
- Using LLM-as-judge without ever checking it against human ratings — an unvalidated judge can be confidently wrong.
- Treating an eval as a one-time gate instead of a regression suite — the next prompt tweak ships unchecked.
