# Command: Create User Story

Reusable prompt for turning a feature or request into a clean user story with acceptance criteria.

## Prompt

```
Act as a senior product manager. Using the provided context, write:

1. A primary user story in the form: "As a [user], I want [capability], so that [outcome]."
2. Up to 3 secondary user stories in the same format, if relevant.
3. Acceptance criteria for the primary story, written as a checklist a QA engineer could test against directly.
4. Edge cases the acceptance criteria should explicitly cover (error states, empty states, permission boundaries).

Do not include implementation detail (no API names, no database fields) — this is a product-level story, not a technical spec.

Context: [PASTE YOUR FEATURE CONTEXT HERE]
```

## When to use this

Breaking a scoped feature (from create-prd.md) into stories ready for an engineering backlog.

## Inputs to paste in

- The feature or capability being broken into stories
- The primary user/persona (see settings/personas.md)
- Any known edge cases already identified
