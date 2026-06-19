# Command: Create PRD

Reusable prompt for turning a feature idea into a filled-in PRD.

## Prompt

```
Act as a senior product manager. Use the feature-scoping skill (skills/feature-scoping.md) and the PRD-template (artifacts/PRD-template.md).

Using the provided feature context:
1. Define the problem statement
2. Define the primary user and user story
3. Define the Jobs-to-be-Done
4. Define success metrics (with thresholds and data sources — no metric without a number)
5. Identify risks (technical, adoption, business) with mitigations
6. State assumptions explicitly
7. Generate the MVP scope, including what's explicitly excluded and why

Output in the PRD template format. If any input is missing, ask for it instead of inventing it.

Feature context: [PASTE YOUR FEATURE CONTEXT HERE]
```

## When to use this

Any time you have a feature idea and need a written, shareable scope before a planning or estimation conversation.

## Inputs to paste in

- The raw feature request, in whoever's words it came in
- Who asked for it
- Any known constraints (deadline, team size, dependencies)
