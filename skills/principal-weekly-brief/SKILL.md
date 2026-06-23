---
name: principal-weekly-brief
description: Use this skill to turn a family office principal's calendar items, open decisions, investment updates, operational issues, travel notes, and pending follow-ups into a concise, decision-ready weekly briefing. Produces a structured brief with an executive summary, decisions needed, meetings, investment items, operational issues, risks, and suggested follow-ups.
---

# Principal Weekly Brief

## Purpose

This skill prepares a concise weekly briefing for a family office principal. It takes the raw, scattered inputs of the week — calendar, open decisions, investment updates, operational issues, travel, and pending follow-ups — and organizes them into a single, decision-ready document the principal can read quickly and act on. It saves the chief of staff or operator hours of assembly while keeping every fact subject to human verification.

## When to use this

- Preparing the recurring Monday (or start-of-week) brief for a principal.
- Consolidating updates from multiple sources into one document before a principal check-in.
- Catching a principal up after travel or time away.
- Standardizing how the office briefs its principal so nothing important is missed week to week.

## Inputs

Provide as much of the following as you have. The skill works with partial inputs and will flag what is missing.

- **Calendar items** for the week (meetings, calls, travel, deadlines).
- **Open decisions** awaiting the principal, with any context and timing.
- **Investment updates** (manager notes, capital calls, portfolio items) — for summary only.
- **Operational issues** (office, household, entity, vendor, administrative).
- **Travel notes** relevant to the week.
- **Pending follow-ups** carried over from prior weeks.
- **Any priorities** the principal has flagged.

## Output

Produce a structured brief with these sections, in this order:

1. **Executive summary** — 3–6 sentences on what matters most this week.
2. **Decisions needed** — table: decision, context, needed-by, owner.
3. **Upcoming meetings** — table: date, meeting, attendees, objective, prep status.
4. **Investment items** — table: item, update, action/decision, status (summary only, no recommendation).
5. **Operational issues** — table: issue, detail, owner, status.
6. **Risks or delays** — table: risk/delay, impact, next step, owner.
7. **Suggested follow-ups** — checklist with owners and dates.
8. **Open questions / missing information** — anything needed to complete the brief.

Use the [weekly family office brief template](../../templates/family-office-brief-template.md) as the output structure.

## Instructions

- Lead with what matters most; the executive summary should let a busy principal grasp the week in under a minute.
- Be concise and concrete. Prefer tables and short lines over prose.
- Use only the information provided. Do not invent meetings, figures, names, or context.
- Clearly distinguish **confirmed information** from **assumptions**. Mark inferred items *(assumption)*.
- Where a field is unknown (an owner, a date, a meeting objective), mark it *(missing)* rather than guessing.
- Summarize investment items neutrally. Do not recommend buying, selling, holding, or allocating.
- Keep the principal in control: frame decisions and follow-ups as items for the principal's judgment, not as actions taken.
- Preserve confidentiality; do not add external detail or speculate about people.

## Quality control

- **Missing information:** If key inputs are absent (e.g., no meeting objectives, no owners), list them under *Open questions / missing information* and do not fabricate them.
- **Hallucination risk:** Every meeting, figure, date, and name must trace to an input. If it is not in the inputs, it does not go in the brief. Re-read the output and remove any detail you cannot source.
- **Confidentiality:** Do not introduce information beyond what was provided. Do not infer sensitive personal detail.
- **Uncertainty:** When something is ambiguous, mark it *(assumption)* or raise it as a question rather than presenting it as fact.

## Do not

- Do not invent meetings, figures, decisions, or context.
- Do not make investment, legal, tax, or compliance recommendations.
- Do not approve a decision or state that a decision has been made unless the input says so.
- Do not draft or send any external communication.
- Do not present assumptions as confirmed facts.
- Do not omit the *missing information* section when inputs are incomplete.

## Example request

> "Using the principal-weekly-brief skill, prepare this week's brief. Here are my inputs: [paste calendar items, open decisions, investment updates, operational issues, travel notes, and pending follow-ups]."

---

*This skill supports human judgment and produces an unverified draft for review. It does not provide investment, legal, tax, accounting, or compliance advice, and it does not make, approve, or authorize any decision, transaction, or communication. A competent person must verify all output before it is used.*
