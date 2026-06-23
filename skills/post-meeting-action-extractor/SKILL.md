---
name: post-meeting-action-extractor
description: Use this skill to convert raw meeting notes into clear decisions, action items, owners, deadlines, and dependencies, plus an internal follow-up draft for human review. Produces a structured record so meetings turn into reliable follow-through.
---

# Post-Meeting Action Extractor

## Purpose

This skill turns raw, messy meeting notes into a clean, structured record of what was decided and what happens next. It extracts decisions, action items, owners, deadlines, and dependencies, and prepares an internal follow-up draft for a person to review and send. It converts meetings into reliable follow-through and durable institutional memory. It does not send anything itself.

## When to use this

- Immediately after a meeting, to turn notes into an owned action list.
- Building a consistent record of decisions and follow-ups across meetings.
- Preparing a follow-up summary for a person to review, edit, and send.
- Capturing institutional memory — what was decided and why.

## Inputs

Provide whatever you have; the skill works with partial notes and flags gaps.

- **Raw meeting notes** (bullet points, transcript excerpts, or rough text).
- **Attendees** and, if known, who owns what area.
- **Meeting context** (title, date, purpose) if not obvious from the notes.
- **Any known deadlines** referenced in or around the meeting.

## Output

Produce a record with these sections, in this order:

1. **Decisions made** — table: decision, context, decided by.
2. **Action items** — table: action, owner, deadline, dependencies, status.
3. **Follow-up message draft** — an internal draft summarizing decisions and actions, for human review and sending.
4. **Open questions** — items raised but not resolved.
5. **Missing information** — actions without a stated owner or deadline.

Use the [action item template](../../templates/action-item-template.md) as the output structure.

## Instructions

- Extract only what the notes support. Do not invent decisions, owners, deadlines, or actions.
- Where the notes do not specify an **owner or deadline, mark it *(missing)*** — never assume one.
- Distinguish **decisions** (settled) from **discussion** (raised but not concluded). Put unresolved items under *Open questions*.
- Separate **confirmed facts** from **assumptions.** Mark inferred items *(assumption)*.
- Keep action items concrete and verb-led ("Send X to Y," "Confirm Z with counsel").
- The follow-up draft is **internal only** — clearly labeled as a draft for human review and editing before any send. The skill never sends.
- Preserve confidentiality; do not add detail beyond the notes.

## Quality control

- **Missing information:** Notes are often incomplete. Every action without a clear owner or deadline must be flagged, not guessed.
- **Hallucination risk:** Do not create action items, decisions, or commitments that are not in the notes. Re-read and remove anything you cannot trace to the source.
- **Confidentiality:** Do not introduce outside information. The follow-up draft must not include detail the notes do not support.
- **Uncertainty:** If it is unclear whether something was decided or merely discussed, treat it as an open question, not a decision.

## Do not

- Do not invent decisions, action items, owners, or deadlines.
- Do not send the follow-up message or any communication.
- Do not assign owners or deadlines the notes do not state.
- Do not make investment, legal, tax, or compliance recommendations.
- Do not record a decision as made if the notes only show discussion.

## Example request

> "Using the post-meeting-action-extractor skill, turn these notes into decisions and action items, and draft an internal follow-up: [paste raw meeting notes and attendees]."

---

*This skill supports human follow-through and produces an unverified draft for review. It does not provide investment, legal, tax, accounting, or compliance advice, and it does not send communications or authorize any decision or transaction. The follow-up draft is internal only and must be reviewed and sent by a person. A competent person must confirm all decisions, owners, and deadlines before they are used.*
