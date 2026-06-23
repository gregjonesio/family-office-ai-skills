---
name: meeting-prep-pack
description: Use this skill to prepare a structured meeting brief from prior notes, attendee details, agenda, open issues, and desired outcomes. Produces a meeting prep pack with the objective, attendees, relevant background, open items, suggested questions, desired outcomes, and materials to review beforehand.
---

# Meeting Prep Pack

## Purpose

This skill assembles a structured meeting brief so a principal or operator walks into a meeting fully prepared. It pulls together prior notes, attendee context, the agenda, open issues, and desired outcomes into a single, concise pack. It standardizes preparation so meetings are productive and nothing important is overlooked. The output is preparation material for human use; it commits the office to nothing.

## When to use this

- Preparing a principal or operator for a counterparty, manager, advisor, or vendor meeting.
- Standardizing how the office prepares for recurring or high-stakes meetings.
- Pulling scattered prior notes and context into one brief before a discussion.
- Ensuring the right questions and desired outcomes are defined in advance.

## Inputs

Provide whatever you have; the skill works with partial material and flags gaps.

- **Meeting basics:** title, date/time, format (in person / call / video).
- **Attendees:** names, roles, affiliations, relevance.
- **Agenda** or the purpose of the meeting.
- **Prior notes / history** with these parties or on this topic.
- **Open items** or unresolved questions.
- **Desired outcomes** for the meeting.

## Output

Produce a pack with these sections, in this order:

1. **Meeting objective** — why the meeting is happening and what a good outcome looks like.
2. **Attendees** — table: name, role/affiliation, relevance, notes.
3. **Relevant background** — concise context from prior notes and history.
4. **Open items** — table: item, status, notes.
5. **Suggested questions** — specific questions to raise.
6. **Desired outcomes** — what the attendee wants to leave with.
7. **Materials to review beforehand** — checklist of documents/items and why.

Include an *Open questions / missing information* note if inputs are incomplete. Use the [meeting prep template](../../templates/meeting-prep-template.md) as the output structure.

## Instructions

- Use only the information provided. Do not invent attendee backgrounds, history, or context.
- Lead with the objective so the brief is immediately useful.
- Make *Suggested questions* specific to this meeting and these parties — not generic.
- Separate **confirmed facts** from **assumptions.** Mark inferred items *(assumption)*.
- Where attendee detail, history, or objectives are unknown, mark them *(missing)* rather than fabricating.
- Keep it concise; a prep pack should be skimmable in a few minutes.
- Do not speculate about people beyond what the inputs support.

## Quality control

- **Missing information:** If the objective, attendee roles, or desired outcomes are not provided, flag them rather than inventing them.
- **Hallucination risk:** Do not supply biographical detail, prior-meeting facts, or relationship history not present in the inputs. Attendee backgrounds in particular must trace to provided material.
- **Confidentiality:** Do not introduce outside information about attendees or their organizations.
- **Uncertainty:** Mark anything inferred as *(assumption)* and surface ambiguity as an open question.

## Do not

- Do not invent attendee backgrounds, prior history, or context.
- Do not make investment, legal, tax, or compliance recommendations.
- Do not commit the office or attendee to any position.
- Do not draft external communications to attendees.
- Do not present assumptions as confirmed facts.

## Example request

> "Using the meeting-prep-pack skill, prepare a brief for this meeting: [paste meeting basics, attendees, agenda, prior notes, open items, and desired outcomes]."

---

*This skill supports human judgment and produces an unverified preparation draft for review. It does not provide investment, legal, tax, accounting, or compliance advice, commits the office to no position, and does not authorize any decision, transaction, or communication. A competent person must verify all output before it is used.*
