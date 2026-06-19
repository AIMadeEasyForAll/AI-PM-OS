# Command: Generate Roadmap

Reusable prompt for turning a prioritized backlog into a shareable roadmap.

## Prompt

```
Act as a senior product manager. Use the roadmap skill (skills/roadmap.md) and the roadmap-template (artifacts/roadmap-template.md).

Using the provided prioritized backlog and capacity:
1. Group items into themes (the outcome being pursued), not a flat feature list
2. Assign each item a confidence level: Committed, Likely, or Exploratory — and don't date anything Exploratory
3. Place items into Now / Next / Later based on confidence and capacity
4. Write an explicit "not on this roadmap" section for anything notable that was considered and cut
5. Set a next review date

Output in the roadmap template format. Use the audience specified below to choose the level of detail (leadership/customer view = Now/Next/Later only; engineering view = include dated swimlanes if dates exist).

Audience: [LEADERSHIP / ENGINEERING / CUSTOMER]
Backlog and capacity: [PASTE PRIORITIZED BACKLOG AND TEAM CAPACITY HERE]
```

## When to use this

Quarterly or half-year planning, or ahead of a leadership review.

## Inputs to paste in

- Output of the prioritization skill (ranked, scoped backlog)
- Team capacity for the period
- Any fixed dates (compliance, partner commitments, exec demos)
- Target audience for this version of the roadmap
