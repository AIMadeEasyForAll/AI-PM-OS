# PRD: Saved Posts Resurfacing

**Status:** Draft
**Owner:** [Name]
**Last updated:** 2026-06-21

## Problem statement

LinkedIn members who save posts to read or act on later have no way to be reminded of them, so saved content gets buried and forgotten — undermining the value of the save action and any intent the member had to return to it.

*Note: this is currently a hypothesis, not yet evidence-backed — see Assumptions.*

## User story

As a LinkedIn member who saves posts to read or act on later, I want to be reminded of posts I've saved, so that I actually revisit and act on the content I intended to come back to.

**Secondary stories:**
- As a LinkedIn member with many saved posts, I want reminders to be selective rather than exhaustive, so that resurfacing doesn't feel like another inbox to manage.

## Jobs-to-be-Done

- **Functional job:** Get prompted to return to content saved earlier, at a moment when it's still useful.
- **Emotional job:** Feel that saving something is worthwhile — not "I'll never see this again."
- **Social job:** Not applicable — this is a private utility action, not a social one.

## Success metrics

| Metric | Type (primary/guardrail) | Threshold | Window | Data source |
|---|---|---|---|---|
| % of saved posts revisited after a reminder | Primary | [NEEDS DATA — no baseline yet] | 7 days post-reminder | Product analytics |
| Click-through rate on resurfacing prompt | Primary | [NEEDS DATA] | Per prompt sent | Product analytics |
| Save rate (posts saved per active user) | Guardrail | No decrease vs. pre-launch baseline | 6 weeks post-launch | Product analytics |
| Reminder opt-out / mute rate | Guardrail | [NEEDS DATA — set after baseline notification fatigue data is reviewed] | 6 weeks post-launch | Notification settings data |

## MVP scope

**In scope:**
- A periodic resurfacing prompt (e.g., in-app module: "You saved N posts — revisit them") for posts saved but not reopened within a set window.
- Basic frequency capping to avoid repeat-nagging on the same saved post.

**Explicitly out of scope (and why):**
- Search, folders, or tagging for saved posts — that's a findability problem, not the resurfacing problem this PRD scopes. Worth a separate PRD if discovery surfaces it as the bigger pain point (see `project-a`).
- AI-personalized resurfacing (e.g., ranking which saved post to surface first) — adds complexity before we know resurfacing alone moves the metric.
- Push notifications / email digest channel — MVP starts in-app only; channel expansion is a v2 decision pending opt-out data.

## Risks

| Risk | Type (technical/adoption/business) | Mitigation | Owner |
|---|---|---|---|
| Core problem is unvalidated — "forgotten" may not be the real pain vs. "can't find" | Business | Run lightweight discovery (support ticket review, short user interviews) before committing eng time | [Owner] |
| Reminder fatigue drives notification opt-outs broadly, not just for this feature | Adoption | Frequency cap; monitor opt-out guardrail metric closely post-launch | [Owner] |
| Resurfacing logic (dedup, scheduling) adds backend complexity for an unvalidated bet | Technical | Keep MVP logic simple (time-based, not ML-based) until validated | [Owner] |

## Assumptions

- We are assuming the core unmet need is "forgetting saved content" rather than "can't find saved content" — based on hypothesis, not data.
- We are assuming members want to be proactively reminded rather than relying on self-initiated browsing — needs validation via discovery.
- We are assuming current save volume and notification capacity can absorb a new prompt type without redesigning notification architecture — unconfirmed.

## Open questions

- What's the current baseline: total saves per user, and what % of saved posts are ever reopened? (Needed to set metric thresholds.)
- Has anyone reviewed support tickets, app store reviews, or NPS comments for signal that "forgotten saves" is a real, voiced pain point?
- What's the team size/timeline available for this work?
- Which channel should resurfacing use first — in-app feed module, notification, or email digest?
- Who owns this PRD going forward (currently unassigned)?
