# Blueprint: Weekly Principal Briefing System

A composed system that turns a week's scattered inputs into a reviewed principal briefing, with meeting prep and follow-through wired in. This is a **design pattern**, not an automation — every step produces a draft a person reviews, and nothing is sent, decided, or actioned by the system. Read-only, human-in-the-loop, non-advisory.

---

## Purpose

Give a principal a concise, consistent weekly briefing — plus the meeting prep and follow-ups that surround it — assembled from approved inputs and verified by a competent person before it reaches the principal.

## When to use

- A recurring weekly (or start-of-week) briefing cadence.
- When meeting prep and post-meeting follow-through should connect to the same weekly view.
- When you want one consistent briefing format the office can rely on.

## Inputs

- Calendar items for the week
- Open decisions awaiting the principal
- Investment and operational updates (for summary only)
- Travel notes
- Pending follow-ups carried over
- Prior week's notes and action items

## Context sources

Manual input first; approved read-only connectors where appropriate. Possible sources: calendar, task list, prior weekly notes, an approved project tracker, and meeting notes. Connectors are optional, scoped, and least-privilege. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Skills used

- [Principal Weekly Brief](../skills/principal-weekly-brief/) — the core briefing
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — prep for the week's key meetings
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — folding last week's outcomes into follow-ups

## Workflow sequence

1. Gather inputs (manual or approved read-only retrieval).
2. Run **Post-Meeting Action Extractor** on last week's meeting notes → carried-over follow-ups.
3. Run **Meeting Prep Pack** for the week's key upcoming meetings → prep list.
4. Run **Principal Weekly Brief** consolidating decisions, meetings, updates, risks, and follow-ups.
5. **Human review gate** → verify facts and framing.
6. Deliver the reviewed brief to the principal (by a person).

## Human review gates

- **Gate 1 — Inputs:** confirm sources are approved and contain no unapproved confidential material.
- **Gate 2 — Pre-delivery:** a competent person verifies every fact, date, and figure against source, confirms assumptions are labeled and missing items flagged, and edits framing.
- **Gate 3 — Delivery:** a person delivers the brief; the system never sends it.

## Outputs

- Weekly principal brief
- Decisions-needed list
- Upcoming meetings prep list
- Follow-up list

## Measurement metrics

- Briefs produced and delivered on cadence
- Human-review completion rate (target: 100%)
- Correction rate in review (trend)
- Estimated preparation time saved (directional)
- Follow-ups carried over vs. closed

See [measurement-framework.md](../docs/measurement-framework.md). Value figures are directional only.

## Failure modes

- Invented updates or meetings not in the inputs
- Stale carried-over items presented as current
- Decisions shown as final before the principal has decided
- Sensitive material pulled from an unapproved source
- Review skipped under time pressure

## Prohibited actions

- Do not send the brief to the principal automatically.
- Do not include confidential material from unapproved sources.
- Do not invent updates.
- Do not mark decisions as final without review.
- No investment, legal, tax, or compliance advice; no recommendations.

## Implementation notes

Start fully manual. Add one read-only context source (e.g., calendar) only after the manual version is trusted. Keep the review gate non-negotiable, especially on busy weeks. Tune inputs when the same correction recurs.

---

*This blueprint is an operational design pattern, not legal, compliance, investment, or fiduciary advice, and not a live integration. Every output is an unverified draft requiring human review.*
