# Playbook: Board & Committee Meeting Preparation

How a family office prepares for recurring governance meetings — board, investment committee, advisory board, or family council — against an annual board calendar: assembling the board book ahead of a pre-read deadline, running routine items through a consent agenda, and turning the meeting into accurate minutes and a tracked action log, without overstating what was decided. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, board, committee, or meeting. Nothing here is investment, legal, tax, or fiduciary advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Run governance meetings on a reliable cadence with complete, well-organized materials and disciplined follow-through: directors receive the board book far enough ahead to arrive prepared, routine matters clear efficiently through a consent agenda, decisions are recorded accurately in minutes that stand as the legal record, and action items leave with owners and dates in a log carried meeting to meeting.

## Operating Problem

Governance meetings carry weight: they set policy, approve actions through resolutions, and create a record that counsel, auditors, and successors rely on. Preparing for them means pulling prior minutes, the open-action log, supporting documents, and agenda topics into a coherent board book, then capturing what was actually decided afterward. A lean office does this by hand under deadline, and the recurring failures are familiar — a board book that lands the night before so directors are unprepared and decisions get deferred, minutes that overstate or understate what was decided (a governance and legal exposure), and action items that evaporate so the same issues resurface every quarter. The discipline a mature board imposes is a standing annual calendar, a fixed pre-read window, and a minutes process owned by the secretary and reviewed by counsel.

## Typical Trigger

A scheduled board, committee, or council meeting on the annual governance calendar — which places standing items by quarter (for example, audit and tax matters early in the year, strategy and budget later) — plus the lead time the office reserves to assemble the board book.

## Frequency

Periodic and scheduled — commonly quarterly for boards and committees, with interim or special meetings as matters require.

## Primary Stakeholders

- **Chief of staff / COO (owner)** — assembles the board book, manages the calendar, and coordinates the post-meeting record.
- **Chair** — sets the agenda and runs the meeting; decides what is consent vs. discussion.
- **Directors / members** — the readers and decision-makers; independent directors where the structure provides for them.
- **Corporate secretary / counsel** — owns the formal minutes and resolutions and confirms quorum and proper authorization. The office's notes support but never replace them.
- **Principal** — participant and, often, the convening authority.

## Required Inputs

- The annual governance calendar and the meeting's agenda
- Prior meeting minutes and the open-action log
- Supporting documents and reports for each agenda item
- Draft resolutions and any items requiring a vote (e.g., banking signatories, related-party approvals)
- Attendee details, roles, and any conflicts to be disclosed
- Desired outcomes for each agenda item

Provide sensitive governance documents manually after review.

## AI-Assisted Activities

- Assemble a structured board book and per-item brief from prior minutes, the action log, the agenda, and desired outcomes with [Meeting Prep Pack](../skills/meeting-prep-pack/).
- Produce plain-English reads of dense supporting documents with [Document Digest](../skills/document-digest/), surfacing key terms, figures, and questions.
- After the meeting, convert notes into decisions, owners, deadlines, and dependencies with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — flagging anything ambiguous rather than inventing a decision.
- Surface open governance items and upcoming agenda obligations in the [Principal Weekly Brief](../skills/principal-weekly-brief/) between meetings.

AI assembles and structures. It commits the office to no position, makes no governance determination, and drafts no formal minutes or resolutions.

## Human Responsibilities

- Maintain the annual calendar so standing items appear in the right quarter and nothing lapses.
- Confirm the board book is complete and accurate and distribute it by the pre-read deadline.
- Decide what belongs on the consent agenda versus full discussion (the chair's call).
- Verify the post-meeting record against what was actually decided and resolve every flagged ambiguity.
- Own the formal minutes and resolutions through the secretary or counsel, and confirm quorum, conflicts disclosed, and proper authorization for each action.

## Review Gates

1. **Materials gate (pre-read deadline)** — the owner confirms the board book is complete and accurate and distributes it a fixed number of days ahead. A standing pre-read window is itself a control against unprepared decisions.
2. **Quorum-and-authority gate** — the secretary or chair confirms a quorum is present and that each action has a properly framed resolution and any required conflict disclosures before a vote.
3. **Decision-capture gate** — a person verifies the extracted decisions and actions against the meeting; ambiguities the AI flags are resolved by a human, not guessed.
4. **Record gate (secretary / counsel)** — formal minutes and resolutions are owned and finalized by the secretary or counsel and approved at the next meeting; the office's working notes support but do not replace them.

## Outputs

- A structured board book and per-item briefs (draft)
- Plain-English digests of supporting documents (draft)
- A post-meeting decision-and-action record (draft)
- A carried-forward open-action log (draft)

## Risks

- **Overstated decisions** — notes can imply a decision that was not made; the decision-capture gate and explicit ambiguity flags guard against it.
- **Incomplete materials** — a missing document undermines the meeting; the materials gate checks completeness.
- **Confidentiality** — governance materials are highly sensitive; use only approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Advice and authority boundary** — the office's notes are not minutes and carry no governance authority; formal records stay with the secretary or counsel.

## Common Failure Points

- **Late board book.** Materials arrive the night before; directors are unprepared and real decisions slip to the next meeting. *Control:* a fixed pre-read deadline enforced by the chair, with a consent agenda clearing routine items so discussion time goes to what matters.
- **Minutes that misstate the decision.** Over-claiming an approval that did not happen, or under-recording one that did, creates governance and legal exposure. *Control:* minutes owned by the secretary and reviewed by counsel, approved at the next meeting; working notes never substitute.
- **Action items that vanish.** Decisions are made but nothing tracks follow-through, so the same issues recur every quarter. *Control:* a standing open-action log carried meeting to meeting with owners and dates.
- **Action without authority.** A decision is taken without a quorum, without a proper resolution, or with an undisclosed conflict. *Control:* the quorum-and-authority gate before any vote, plus a conflicts register.
- **No annual calendar.** Standing obligations (audit sign-off, budget approval, signatory updates) are remembered ad hoc and occasionally missed. *Control:* an annual governance calendar placing each recurring item in its quarter.
- **Consent agenda misused.** A matter needing real discussion is buried in consent and passes without scrutiny. *Control:* the chair's explicit decision on what is consent vs. discussion, with any director able to pull an item.

## Metrics

- Board book distributed by the pre-read deadline (target: every meeting)
- Review-gate completion rate, including minutes and resolutions (target: 100%)
- Action items captured with owner and date vs. dropped
- Open actions carried to closure between meetings
- Standing annual-calendar items completed on schedule

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)
- [Principal Weekly Brief](../skills/principal-weekly-brief/)

## Related Blueprints

- [Meeting-to-Execution System](../blueprints/meeting-to-execution-system.md)

## Related Case Studies

- [Meeting-to-Execution Workflow](../case-studies/meeting-to-execution.md)

## Related Governance Documents

- [Operating Model](../docs/operating-model.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Measurement Framework](../docs/measurement-framework.md)
- [Evaluation and Red-Team Guide](../docs/evaluation-guide.md) and the [Post-Meeting Action evals](../evals/post-meeting-action-evals.md)

## Evolution Path

1. **Ad hoc** — meetings are scheduled as needed, board books assembled last-minute, and decisions captured informally.
2. **Calendared** — an annual governance calendar, a fixed pre-read window, and a consent agenda bring rhythm and preparation; these are governance controls independent of AI.
3. **Recorded** — minutes owned by the secretary and reviewed by counsel, a conflicts register, and a carried open-action log make the record reliable and follow-through accountable.
4. **AI-assisted** — the prep pack assembles the board book and the action extractor builds the post-meeting record; approved, read-only retrieval of prior minutes and the action log seeds the next meeting — a governed data-access change, not new authority.

No stage lets the office's notes become the formal record or lets the AI characterize a decision the meeting did not make. Minutes, resolutions, and quorum stay human and with the secretary or counsel.

---

*This playbook is an illustrative operating pattern, not legal, investment, tax, or fiduciary advice, and not a live integration. It drafts no formal minutes or resolutions and makes no governance determination. Every output described is an unverified draft requiring human review.*
