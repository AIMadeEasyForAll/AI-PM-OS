# Command: Analyze Feedback

Reusable prompt for turning a pile of raw feedback (tickets, interview notes, NPS comments) into a synthesized, falsifiable finding, using the discovery skill.

## Prompt

```
Act as a senior product manager. Use the discovery skill (skills/discovery.md).

Using the provided raw feedback:
1. Group it into themes — name each theme as a specific, falsifiable claim about user behavior or need, not a vague topic label
2. For each theme, cite the specific evidence (quotes, behaviors, counts) that supports it — do not state a theme with fewer than 2 independent sources backing it
3. Flag anything that's a single anecdote, separately, as "not yet a pattern"
4. Recommend, for each confirmed theme, whether it's ready to move into feature-scoping, needs more discovery first, or should be deprioritized
5. Do not invent counts or percentages not present in the source material — if volume matters and isn't given, say so explicitly

Output as a short synthesis: themes (with evidence), single anecdotes (not yet patterns), and a recommendation per theme.

Raw feedback: [PASTE TICKETS, NOTES, OR COMMENTS HERE]
```

## When to use this

Whenever feedback has piled up across channels (support, sales, interviews) and needs to turn into something actionable rather than just summarized.

## Inputs to paste in

- The raw feedback — tickets, interview notes, survey comments, NPS verbatims
- The time window this feedback covers
- Any existing hypothesis you're testing it against
