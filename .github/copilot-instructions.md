# Copilot Instructions

This repository supports product management workflows: scoping, evaluation, roadmapping, and stakeholder communication for product features — most of them AI-powered features specifically.

## When generating content

- Prefer markdown over plain text or code blocks, unless generating an actual code sample.
- Use concise language. Cut filler — "in order to" becomes "to," "utilize" becomes "use."
- Include acceptance criteria on anything that resembles a requirement or user story.
- Include measurable outcomes on anything that resembles a feature or initiative. If a metric isn't given, flag it as missing rather than inventing one.
- Use product management terminology consistently: JTBD, MVP, north star metric, leading/lagging indicator, definition of done.
- Never invent metrics, dates, percentages, or user counts. If the source material doesn't contain a number, leave a placeholder like `[NEEDS DATA]` instead of fabricating one.

## Context to apply

Before generating an artifact, check `settings/business-context.md`, `settings/personas.md`, and `settings/product-principles.md` in this repository for context that should shape the output. Treat these as binding constraints, not optional background.

## Templates

When the task matches an existing template in `artifacts/` (PRD, evaluation plan, experiment brief, decision log, launch checklist, roadmap), follow that template's structure rather than generating a new format from scratch.
