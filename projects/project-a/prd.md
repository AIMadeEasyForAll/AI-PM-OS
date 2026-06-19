# PRD: Saved Posts Redesign

**Status:** Draft
**Owner:** [Your name]
**Last updated:** 2026-06-19

## Problem statement

Users save posts intending to revisit them, but the current Saved Posts list is an undifferentiated, reverse-chronological feed with no way to organize or re-find a specific item — so saved posts go unread and the feature stops getting used after the first few saves.

## User story

As a member who saves posts to read or reference later, I want to organize and quickly re-find what I've saved, so that saving something is actually useful instead of becoming a junk drawer.

**Secondary stories:**
- As a member, I want to remove items I've already read from view without permanently deleting them, so my list stays relevant.
- As a member, I want to search within my saved posts, so I can find a specific one without scrolling.

## Jobs-to-be-Done

- **Functional job:** Retrieve a specific previously-seen post quickly, without re-searching the feed.
- **Emotional job:** Feel in control of information they intended to come back to, rather than anxious about losing track of it.

## Success metrics

| Metric | Type | Threshold | Window | Data source |
|---|---|---|---|---|
| Saved-post revisit rate (% of saves opened again within 30 days) | Primary | +20% relative to current baseline | 6 weeks post-launch | Product analytics |
| Save rate (saves per active user per week) | Guardrail | No more than 5% decline | 6 weeks post-launch | Product analytics |

## MVP scope

**In scope:**
- Folder/collection-based organization for saved posts (user-created, manual assignment)
- Search within saved posts by keyword
- Mark-as-read state that filters the default view without deleting the item

**Explicitly out of scope (and why):**
- Auto-categorization of saves by topic — requires a classification model and eval plan (see `skills/ai-evaluation.md`); deferred until manual organization is validated as the right mental model.
- Sharing or collaborative saved collections — no validated demand yet; revisit after discovery.

## Risks

| Risk | Type | Mitigation | Owner |
|---|---|---|---|
| Users don't adopt manual folders (too much setup friction) | Adoption | Ship a single default "Unsorted" folder so organizing is optional, not required, to get value | [Owner] |
| Search index latency on large saved-post lists | Technical | Cap initial release to lists under 500 items; monitor query latency before removing the cap | [Owner] |

## Assumptions

- We are assuming the low revisit rate is caused by poor organization rather than the underlying posts no longer being relevant by the time users return — based on support tickets describing "I can never find what I saved," not yet confirmed via direct user interviews.

## Open questions

- Should folders be visible to other users viewing a profile, or private by default? Leaning private — needs a decision before design starts.
- Is 500 saved items a realistic cap, or do power users exceed this regularly? Needs a data pull before launch.
