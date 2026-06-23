# Post-Meeting Action Extractor

A skill that turns raw meeting notes into a clean, structured record — decisions, action items, owners, deadlines, and dependencies — plus an internal follow-up draft for a person to review and send.

## What it does

Produces a record: decisions made, action items with owners and deadlines, an internal follow-up draft, open questions, and a list of any actions missing an owner or deadline.

## Who uses it

Operators, chiefs of staff, and executive assistants who need meetings to turn into reliable follow-through.

## How to use it

1. Paste your raw notes and attendees (see [SKILL.md](SKILL.md) → *Inputs*). Provide only sanitized material.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Review the record; **confirm owners and deadlines** and fill anything marked *(missing)*.
4. Edit the follow-up draft and send it yourself — **the skill never sends.**

## What it will not do

- It will not invent decisions, owners, or deadlines.
- It will not send the follow-up or any communication.
- It will not record discussion as a decision.

## Files

- [SKILL.md](SKILL.md) — the workflow contract.
- [examples/sample-input.md](examples/sample-input.md) — fictional raw meeting notes.
- [examples/sample-output.md](examples/sample-output.md) — the structured record produced from them.

*Output is a draft for human review. The follow-up draft is internal and must be reviewed before sending. Not investment, legal, tax, or compliance advice.*
