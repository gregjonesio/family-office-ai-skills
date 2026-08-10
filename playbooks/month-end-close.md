# Playbook: Month-End Close

How a family office keeps its books current month by month: working transaction queues to a resolved state rather than an empty one, holding cutoff, reconciling every cash and card account, tying intercompany both ways, and passing a reviewer gate, so that the quarter is a review rather than a rescue. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, entity, ledger, statement, or account. Nothing here is accounting, tax, audit, or financial advice, performs no reconciliation, and books no entry. Every AI output described is an unverified draft requiring human review.

---

## Objective

Finish each month with books that a person has actually reconciled, an aged list of what remains open, and a reviewer who has looked at the work. The measure is not that the month was processed. It is that every account ties to independent evidence, every open item has an owner and an age, and nothing was resolved by inference.

## Operating Problem

The monthly close is where a family office either stays current or quietly falls behind, and falling behind is rarely announced. Queues get emptied rather than resolved. Transactions land in the month they were noticed rather than the month they occurred. Recurring entries keep posting after the arrangement behind them changed. Intercompany drifts because nobody ties it until quarter end, by which point three months of movement have to be untangled at once.

None of that produces an error message. The books look processed. The damage surfaces a quarter later as a balance nobody can explain, and by then the source documents are cold and the person who made the call has forgotten why.

The discipline that prevents it is unglamorous: a fixed monthly cadence, a queue worked to a *resolved* state with reasons recorded, a hard cutoff, reconciliation against evidence from outside the ledger, and a reviewer who is not the preparer. An office that closes small and often turns the quarter into a review. An office that defers turns the quarter into an investigation.

## Typical Trigger

The month-end date, plus arrival of the period's bank, card, and custodial statements. In offices carrying investment positions, the month closes on available information and the lagged values are trued up at the quarter, not held open.

## Frequency

Monthly. The quarter adds procedures on top of this cadence rather than replacing it. See [Quarter-End Close](quarter-end-close.md).

## Primary Stakeholders

- **Bookkeeper or controller (preparer):** works the queues, prepares entries, performs reconciliations, and carries the open-item list.
- **Controller or CFO (reviewer):** reviews against evidence rather than against the preparer's summary, and owns the conclusion.
- **Outside CPA or business manager:** provides the independent review where the office is too lean to separate preparer from reviewer internally.
- **Principal or family CFO:** consumes the result; sees a monthly position and is told what is unresolved, not only what is finished.

## Required Inputs

- Bank, card, and custodial statements for the period, obtained from the institution rather than from the accounting platform
- The transaction queues for every account, including items deliberately left unresolved last month
- The office's written conventions: chart of accounts, categorization rules, allocation policy, intercompany policy, tolerances, and any hard date floor. See [standing-context.md](../docs/standing-context.md)
- Recurring and accrual schedules, with the arrangement each one rests on
- Prior month's open items and reconciling items, with their original dates
- Intercompany balances for every entity pair

Statements and account detail are highly sensitive; provide them manually in approved environments only.

## AI-Assisted Activities

- Establish what is already recorded before any entry is prepared, with [Pre-Booking Gap Analysis](../skills/pre-booking-gap-analysis/). The output is a coverage classification of the period's activity and a draft packet limited to the genuinely missing population.
- Where activity spans several accounts, group it first with [Transfer and Duplicate Review](../skills/transfer-duplicate-review/), so one movement is not recorded twice. Cross-entity movements are escalated to the controller, never resolved by the skill.
- Assemble each account reconciliation with [Reconciliation Evidence Pack](../skills/reconciliation-evidence-pack/): completeness and validity tested separately, an aged reconciling-item schedule, and gross movements stated before any net.
- After entries are recorded, confirm they landed with [Post-Write Verification](../skills/post-write-verification/), using evidence read back through a path other than the one that recorded them.
- Read statements, notices, and supporting documents into plain English with [Document Digest](../skills/document-digest/), without performing accounting or rendering advice.
- Carry the open-item list forward with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) used as a checklist extractor, so items keep their original dates and visibly age.

None of these reconcile, book, allocate, eliminate, or close. They classify candidates and assemble evidence. **The preparer prepares, the reviewer concludes, and a person closes the period.** A pack reporting a zero difference has not reconciled anything, and an entry the platform reports as recorded is not recorded until it has been independently observed.

## Human Responsibilities

- Decide every categorization the written conventions do not already answer, and add the new convention rather than deciding it again next month.
- Hold cutoff: an item belongs to the period in which it occurred, not the period in which it surfaced.
- Confirm each recurring entry still matches the arrangement behind it before it posts again.
- Perform the reconciliations and reach the conclusion.
- Tie every intercompany pair both ways, in the same session.
- Decide what is genuinely unresolved and communicate it, rather than closing over it.

## Review Gates

1. **Cutoff gate:** confirm the period's boundaries and that no activity outside the hard date floor has been drawn in.
2. **Resolution gate:** every queue item is resolved *with a reason*, not merely categorized. An item cleared to empty the queue has not been resolved.
3. **Reconciliation gate:** a competent person reconciles every cash and card account against evidence obtained independently of the ledger.
4. **Intercompany gate:** each entity pair ties both ways. A balance that ties on one side proves nothing about the other.
5. **Preparer and reviewer gate:** a reviewer independent of the preparer checks the work against source evidence, not against the preparer's summary. Where internal separation is impossible, the review is external or the limitation is written down.
6. **Close gate:** a person closes the period and states what remains open. The AI never closes a period.

## Outputs

- A resolved transaction population with reasons recorded (draft)
- Reconciliation evidence for each account, with an aged reconciling-item schedule (draft)
- An intercompany tie-out by entity pair (draft)
- An open-item list carrying original dates and owners (draft)
- New or changed conventions captured for the office's written record (draft)

## Risks

- **The empty queue.** A queue at zero looks finished and may only mean everything was assigned somewhere. Resolution is the standard, not emptiness.
- **Inference filling gaps.** Where a convention does not exist, a plausible answer is worse than an escalation, because it will be applied consistently and wrongly.
- **Reviewer reading the summary.** A review performed against the preparer's own account of the work is not an independent control.
- **Overreliance:** an orderly checklist can imply the work is sound; reconciliations, conclusions, and the close stay human.
- **Confidentiality:** financial detail is highly sensitive; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **The queue is emptied rather than resolved.** Every item is categorized, the queue reads zero, and a portion was guessed. *Control:* require a reason per item, and treat items resolved without a convention as escalations rather than completions.
- **Cutoff drifts.** Items are booked in the month they were noticed. Comparability across months quietly degrades. *Control:* an explicit cutoff gate and a stated date floor.
- **Recurring entries outlive their arrangement.** A monthly entry keeps posting after the underlying agreement changed or ended. *Control:* confirm each recurring entry against its source arrangement on a stated cadence, and record what it rests on.
- **Intercompany is only tied at the quarter.** Three months of drift must be untangled at once, usually under deadline. *Control:* a monthly reciprocal tie-out by entity pair.
- **"Booked through" is recorded as fact.** A note says the month was processed, which records intent rather than effect. *Control:* verify the state of the account, not the completion of the task.
- **Reconciling items age invisibly.** An item carried forward each month keeps its status and loses its age. *Control:* age every reconciling item from the date it arose, never from the current period end.
- **A closed period is reopened silently.** A late entry lands in a period already reported. *Control:* a period lock, and a stated procedure for who can reopen and what gets reissued.
- **The month closes with no one looking across months.** Each period is internally consistent and the trend is never examined. *Control:* a month-over-month comparison as part of the review gate.

## Metrics

- Months closed within the office's stated window
- Queue items resolved with a recorded reason, as a share of items worked
- Reconciliations completed against independent evidence, by account
- Intercompany pairs tied both ways each month
- Age profile of open reconciling items, watched as a distribution rather than a count
- New conventions captured per month, which should fall over time

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Pre-Booking Gap Analysis](../skills/pre-booking-gap-analysis/)
- [Transfer and Duplicate Review](../skills/transfer-duplicate-review/)
- [Reconciliation Evidence Pack](../skills/reconciliation-evidence-pack/)
- [Post-Write Verification](../skills/post-write-verification/)
- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

This playbook composes skills directly rather than through a single blueprint. For the layered design it sits within, see the [Reference Architecture](../docs/reference-architecture.md).

## Related Case Studies

- [Capital Call Processing](../case-studies/capital-call-processing.md): capital activity that lands in a month and must be recorded once.

## Related Governance Documents

- [Standing Context](../docs/standing-context.md)
- [Action Authority Model](../docs/action-authority-model.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Reactive.** The month is worked when someone notices it has not been. Queues carry unknown age, cutoff is whenever the work happened, and one person prepares and checks.
2. **Cadenced.** A fixed monthly window, a standing reconciliation set, and a written cutoff. These disciplines stand entirely independent of AI and deliver most of the benefit.
3. **Documented conventions.** Recurring decisions are written down with their scope and reason, so the same question is not re-decided monthly and a new preparer reaches the same answer. See [standing-context.md](../docs/standing-context.md).
4. **Independently reviewed.** A preparer and reviewer separation against source evidence, backstopped externally where the office is too lean, plus a period lock.
5. **AI-assisted.** Coverage classification before preparation, evidence assembly for reconciliation, and independent post-write verification. A governed change in how evidence is prepared, not a change in who decides.

No stage lets the AI reconcile, book entries, tie intercompany, or close a period. The accounting work, the review, and the close stay human.

---

*This playbook is an illustrative operating pattern, not accounting, tax, audit, or financial advice, and not a live integration. It performs no reconciliation, books no entry, and closes no period. Every output described is an unverified draft requiring human review.*
