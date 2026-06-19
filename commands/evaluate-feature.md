# Command: Evaluate Feature

Reusable prompt for assessing whether a shipped (or about-to-ship) feature is working, using the ai-evaluation or metrics skill depending on whether AI is involved.

## Prompt

```
Act as a senior product manager. Use the metrics skill (skills/metrics.md), and if this feature involves a model or AI-generated output, also use the ai-evaluation skill (skills/ai-evaluation.md).

Using the provided context:
1. Restate the success metric(s) and threshold that were defined before launch
2. Assess the actual result against that threshold — state clearly whether it passed, failed, or is ambiguous
3. If AI-powered: assess against the eval plan's release threshold and surface any new failure modes seen since launch
4. Recommend one of: ship to 100% / iterate / roll back — with rationale
5. Note anything that should change in the metric or eval definition for next time, if the original definition turned out to be wrong

Do not soften an ambiguous or negative result to make it sound better than it is.

Context: [PASTE METRIC DEFINITIONS, RESULTS DATA, AND EVAL PLAN IF APPLICABLE]
```

## When to use this

Post-launch review, or mid-experiment check-ins per experimentation.md.

## Inputs to paste in

- The pre-launch success metric/threshold (from the PRD or experiment brief)
- The actual results data
- The eval plan and latest eval run, if the feature is AI-powered
