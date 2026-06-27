# Case Study: Meeting-to-Execution Workflow

How an operator converts ambiguous meeting notes — with possible decisions, loose follow-ups, and open questions — into a clean execution plan, without treating anything ambiguous as a final decision.

> **Fictionalized and illustrative.** This is a sanitized, generalized example. It does not describe any actual family office, employer, client, principal, meeting, or document. All names, scenarios, and figures are invented and directional. Nothing here is investment, legal, tax, accounting, compliance, or fiduciary advice.

---

## Scenario

A working meeting produces a page of rough notes: some things sound decided, some sound like maybes, several follow-ups have no owner or date, and a few questions were left open. A week later, no one is certain what was actually agreed. The operator needs to turn the notes into a clean execution plan — decisions, owners, deadlines, and open questions — that the team can act on, while being honest about what was decided versus what only seemed to be.

## Operating problem

Meeting notes are ambiguous by nature, and the gap between "discussed" and "decided" is exactly where lean teams drop the ball. Read too aggressively, the plan asserts decisions no one made; read too cautiously, real follow-ups go untracked. A small team has no one to reconcile the notes into a trustworthy plan promptly, so follow-through degrades. The difficulty is extracting structure from ambiguity without manufacturing certainty.

## Traditional workflow

The operator rereads the notes days later, reconstructs intent from memory, types a follow-up list, and guesses at owners and dates where the notes are silent — sometimes promoting a "we should consider" into a firm action, sometimes losing a real commitment in the noise. The plan's reliability depends on how fresh the operator's memory is.

## AI-assisted workflow

The operator runs the [Meeting-to-Execution System](../blueprints/meeting-to-execution-system.md) blueprint:

1. If prep exists, run **[Meeting Prep Pack](../skills/meeting-prep-pack/)** beforehand so the meeting has a structured agenda and the notes map back to intended topics.
2. Run **[Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)** on the raw notes to separate apparent decisions from follow-ups and open questions, assign owners and deadlines **only where the notes support them**, and explicitly flag every missing owner, missing date, and ambiguous item rather than guessing.
3. Run **[Principal Weekly Brief](../skills/principal-weekly-brief/)** to fold the resulting action items and open decisions into the weekly view so they stay visible until closed.

The AI drafts the plan and marks what is uncertain. It does not resolve the ambiguity — a person does that.

## Inputs

- Raw meeting notes (fictional or approved, non-confidential)
- The agenda or prep pack, if one exists
- The attendee list and their roles, as available
- Any prior action items the meeting was meant to advance

## Skills used

- [Meeting Prep Pack](../skills/meeting-prep-pack/) — structuring the meeting beforehand, where possible
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — converting raw notes into decisions, owners, deadlines, and flagged gaps
- [Principal Weekly Brief](../skills/principal-weekly-brief/) — keeping the resulting items visible in the weekly view

## Context sources

Manual input first: the operator pastes the notes and agenda. Approved, read-only retrieval of stored notes may reduce copy-and-paste once trusted. The AI introduces nothing not present in the notes. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Review gates

- **Inputs gate:** confirm the notes are appropriate to process and contain no unapproved confidential information.
- **Decision-vs-discussion gate:** a competent person — ideally an attendee — confirms which items were actually decided and which were only discussed, correcting anything the draft overstated.
- **Ownership gate:** the reviewer assigns or confirms owners and dates for items the notes left open, rather than accepting an AI guess.
- **Pre-circulation gate:** the reviewer verifies the plan reflects what happened before it is shared or acted on.

## Outputs

- A draft execution plan: decisions, follow-ups, and open questions, clearly separated
- An owned action list with owners and deadlines, with gaps flagged (draft)
- A list of items needing confirmation because the notes were ambiguous (draft)
- A weekly-brief entry surfacing the open decisions and actions (draft)

## Measurement

How this workflow could be measured ([measurement framework](../docs/measurement-framework.md); figures are directional, not audited):

- **Time saved** — reconciliation and write-up time avoided per meeting.
- **Cycle time reduced** — from "meeting ends" to "reviewed execution plan ready."
- **Review exceptions** — plans acted on without the required confirmation (driven toward zero).
- **Follow-ups captured** — real commitments tracked rather than lost in the notes.
- **Decisions supported** — ambiguous items correctly escalated for confirmation instead of being assumed.
- **Documents summarized** — sets of raw notes turned into structured plans.
- **Action items created** — owned, dated follow-ups produced.

## Risks and controls

- **Confidentiality** — notes may reference sensitive matters; use only approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Stale information** — a plan built from old notes may miss later changes; the reviewer confirms current status.
- **Hallucination** — the AI may invent an owner, a date, or a decision the notes do not support; the skill flags gaps instead of guessing, and the reviewer confirms.
- **Treating ambiguity as decided** — the core risk here; apparent decisions are labeled as such and confirmed by an attendee before they are treated as final. **Drafts only.**
- **Professional advice boundary** — the plan organizes follow-through; it makes no investment, legal, tax, or compliance recommendation.
- **Overreliance** — a tidy plan reads as authoritative; the reviewer treats it as a draft and confirms the decisions it asserts.

## What remains human

- Confirming what was actually decided versus merely discussed.
- Assigning owners and deadlines the notes did not settle.
- The decisions themselves, and any that need to be re-opened.
- Communicating the plan to the team.
- Final accountability for follow-through.

## Takeaway

The value is honest structure: the AI turns messy notes into a usable plan and, crucially, flags what is uncertain rather than smoothing it over — leaving a person to confirm what was truly decided before anything is treated as final.

---

*This case study is an illustrative operating pattern, not legal, compliance, investment, tax, or fiduciary advice, and not a live integration. Ambiguous notes are not final decisions; every output described is an unverified draft requiring human review.*
