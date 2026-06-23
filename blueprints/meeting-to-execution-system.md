# Blueprint: Meeting-to-Execution System

A composed system that connects meeting preparation to follow-through: prepare the meeting, capture decisions and actions afterward, and roll them into the weekly view — all as reviewed drafts. This is a **design pattern**, not an automation. Read-only, human-in-the-loop, non-advisory. The system never sends, assigns, or updates anything on its own.

---

## Purpose

Close the gap between meetings and execution. Standardize prep so meetings are productive, and convert what was decided into a clean, owned action register that flows into the weekly rollup — with a person reviewing each step.

## When to use

- Recurring or high-stakes meetings where prep and follow-through both matter.
- When decisions and action items routinely get lost after meetings.
- When meeting outcomes should feed a weekly status view.

## Inputs

- Meeting agenda and objective
- Attendees and prior notes
- Raw notes or transcript from the meeting
- Existing task/action items

## Context sources

Manual input first; approved read-only connectors where appropriate. Possible sources: agenda, prior notes, transcript or raw notes, a task list, and a project tracker. Connectors are optional, scoped, least-privilege, and read-only. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Skills used

- [Meeting Prep Pack](../skills/meeting-prep-pack/) — structured prep before the meeting
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — decisions and actions after
- [Principal Weekly Brief](../skills/principal-weekly-brief/) — rolling outcomes into the weekly view

## Workflow sequence

1. Before the meeting: run **Meeting Prep Pack** → objective, background, questions, desired outcomes.
2. **Human review gate** → confirm prep before the meeting.
3. After the meeting: run **Post-Meeting Action Extractor** on the notes → decisions, actions, owners, deadlines, and an internal follow-up draft.
4. **Human review gate** → confirm owners/deadlines; distinguish decisions from discussion.
5. Roll confirmed items into the **Principal Weekly Brief** status view.
6. A person sends any follow-ups and updates any systems.

## Human review gates

- **Gate 1 — Pre-meeting:** confirm prep facts and attendee details.
- **Gate 2 — Post-meeting:** verify which items were actually decided, confirm or fill missing owners and deadlines, and review the follow-up draft.
- **Gate 3 — Send/update:** a person sends follow-ups and updates task systems; the system does neither.

## Outputs

- Meeting prep pack
- Decisions made
- Action register (owners, deadlines, dependencies)
- Follow-up draft (internal, for human sending)
- Weekly status rollup

## Measurement metrics

- Meetings with prep produced
- Action items captured with owner and deadline
- Human-review completion rate (target: 100%)
- Follow-ups closed vs. carried over
- Estimated time saved (directional)

See [measurement-framework.md](../docs/measurement-framework.md). Value figures are directional only.

## Failure modes

- Ambiguous notes treated as firm decisions
- Owners or deadlines invented where the notes are silent
- The follow-up draft sent without review
- Task systems updated without approval
- Prep facts not verified before the meeting

## Prohibited actions

- Do not automatically send follow-ups.
- Do not assign commitments without review.
- Do not treat ambiguous notes as decisions.
- Do not update systems without approval.
- No investment, legal, tax, or compliance advice.

## Implementation notes

Run it manually end-to-end first. The highest-value, highest-risk gate is post-meeting: enforce the rule that anything not clearly decided is an open question, and anything without a stated owner/deadline is flagged, never guessed. Sending and system updates stay human.

---

*This blueprint is an operational design pattern, not legal, compliance, investment, or fiduciary advice, and not a live integration. The follow-up draft is internal and must be reviewed and sent by a person. Every output is an unverified draft requiring human review.*
