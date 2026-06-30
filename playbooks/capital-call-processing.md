# Playbook: Capital Call Processing

How a family office runs an incoming capital call as a controlled payment process — capturing the obligation, routing approvals under an authorized-signer matrix, verifying wiring instructions out of band, releasing funds under dual control, and reconciling to the commitment ledger — with AI making the notice legible and trackable but never touching the money. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, fund, commitment, document, or account. Nothing here approves a payment, initiates a wire, or constitutes legal, tax, or accounting advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Fund each capital call accurately, on time, and to the correct account: capture the amount, due date, and commitment correctly; confirm cash is available with enough lead time; route approvals under the office's signer matrix; verify wiring instructions through an independent channel; release the wire under dual control; and reconcile the draw against the commitment ledger — with no missed date, no misread figure, and no path by which AI or a single person can move funds alone.

## Operating Problem

Capital calls are time-sensitive, infrequent enough that no routine forms around them, and unforgiving of error. Three things make them dangerous in a lean office. First, **wire fraud**: business email compromise (BEC) targeting capital calls is among the most common and costly frauds against family offices, because the attacker only has to alter banking instructions on a single notice. Second, **funding lead time**: the cash often has to be raised — from a capital account, a line of credit, or by selling liquid holdings that settle T+1 or later — so a call discovered late can force a fire sale. Third, **the cost of being late**: most LPAs impose interest, dilution, or in the extreme forfeiture of the interest for a defaulted call. The challenge is reliable, detail-heavy processing under deadline with controls strong enough that no individual — and no AI — can release funds unilaterally.

## Typical Trigger

A capital call notice arrives from a fund the office has committed to, stating an amount due, a due date (commonly 10 business days out, sometimes shorter), wiring instructions, and references to the governing documents.

## Frequency

On receipt — irregular and unpredictable across the commitment's life, often clustered in a fund's early years as it deploys.

## Primary Stakeholders

- **Controller / operations (owner, the "preparer")** — captures the obligation, stages the payment, and completes recordkeeping. Under segregation of duties, the preparer never also releases the wire.
- **Authorized approver(s)** — authorize the payment per the signer matrix and approval thresholds; larger calls require a second approver or the principal.
- **Wire releaser** — a different person who releases the wire in the banking portal under dual control. Preparer ≠ releaser, by design.
- **Fund administrator / GP / counsel** — field questions on ambiguous terms; the administrator is the known channel for verifying banking details.

## Required Inputs

- The capital call notice (fictional or approved, non-confidential)
- The commitment ledger: total commitment, called to date, unfunded balance, recallable distributions
- The office's authorized-signer matrix and approval thresholds (who approves at what amount, who releases)
- Known-good, previously verified banking instructions for the fund on file
- The funding source and its settlement lead time
- Prior call history for the same commitment

Notices carry account and commitment detail; use only approved environments.

## AI-Assisted Activities

- Summarize the notice with [Document Digest](../skills/document-digest/): amount due, due date, the commitment it draws against, references to the governing documents, and precise questions for the administrator or counsel if anything is ambiguous — **without legal or tax advice**.
- Turn the notice into an owned checklist with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) (used here as an obligation-to-action extractor): confirm amount and date, check the unfunded balance, confirm cash availability and lead time, obtain approvals, verify wiring independently, stage and release the wire under dual control, complete recordkeeping.
- Surface the pending call, its due date, and its funding status in the [Principal Weekly Brief](../skills/principal-weekly-brief/) until it is closed.

AI summarizes, structures, and reminds. It does not approve, transcribe wiring details as verified, stage a payment, or initiate anything.

## Human Responsibilities

- Verify the amount and due date against the notice and the commitment ledger, and confirm the call is within the unfunded balance.
- Independently verify wiring instructions through a known channel — a callback to the administrator at a number already on file, never a number or email from the notice itself.
- Confirm cash is available with enough settlement lead time before committing to fund.
- Approve the payment under the signer matrix; release it under dual control with a second person.
- Apply any legal or tax judgment and own final reconciliation and recordkeeping.

## Review Gates

1. **Inputs gate** — confirm the notice is appropriate to process and carries no unneeded confidential data, and that the call is within the committed unfunded balance.
2. **Amount-and-date gate** — a competent person verifies the amount due and due date against the notice and the commitment ledger.
3. **Wire-verification gate (independent, out-of-band)** — a person confirms wiring instructions by callback to a known administrator contact, comparing against the banking details already on file. Any change from the on-file details is treated as presumptive fraud until proven otherwise. Non-negotiable.
4. **Approval gate (signer matrix)** — the required approver(s) authorize per the office's thresholds; calls above the threshold require a second approver or the principal. The AI never approves.
5. **Release gate (dual control / segregation of duties)** — a different person from the preparer releases the wire in the banking portal. No one individual both stages and releases a payment. The system never releases.

## Outputs

- A plain-English summary of the obligation (draft)
- An owned processing checklist: confirm, check unfunded balance, fund, approve, verify wire, release, reconcile, record (draft)
- A weekly-brief entry surfacing the pending call, due date, and funding status (draft)
- A question list for the administrator or counsel, if anything is ambiguous (draft)

## Risks

- **Fraud and payment-control risk** — wiring instructions are a BEC target; verified out of band against on-file details, never trusted from the document, an email, or the AI. See [threat-model.md](../docs/threat-model.md).
- **Stale information** — a remembered amount or banking detail can be wrong; every figure is verified against the current notice and the commitment ledger.
- **Hallucination** — the AI may misread an amount, date, or account reference; all are verified against source.
- **Overreliance** — a clean checklist can create false comfort; the verification, approval, and dual-control release gates remain human.
- **Advice boundary** — outputs are a summary and checklist, not legal, tax, or accounting advice; ambiguities go to counsel or the administrator.
- **Confidentiality** — see [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **Business email compromise.** A fraudster sends or alters a notice with new wiring instructions; the office wires to the fraud account. This is the single most common and most expensive failure. *Control:* out-of-band callback verification to a known administrator contact, and treating any change to on-file banking details as fraud until disproven.
- **No segregation of duties.** One person captures, approves, and releases the wire — the classic single point of both error and fraud. *Control:* preparer ≠ approver ≠ releaser, enforced in the banking portal's user roles, not just on paper.
- **No dual control on release.** A single login can move funds out. *Control:* dual authorization configured at the bank so a second person must release.
- **Notice sits in an inbox.** The call is read late, leaving no time to raise cash or hit the due date. *Control:* a monitored intake and the weekly brief surfacing every open call and its due date.
- **No cash and no lead time.** The office commits to fund without confirming the source settles in time, forcing a liquidation or a missed call. *Control:* a cash-availability check with explicit settlement lead time before funding is staged.
- **Wrong entity funded.** The call belongs to one investment entity but is paid from another, commingling funds and corrupting the books. *Control:* the call is tied to a specific commitment and funding account on the ledger before staging.
- **Reliance on the GP's email as authoritative.** Treating emailed instructions as verified. *Control:* the administrator, via a known channel, is the source of truth — not the inbound message.

## Metrics

- Calls funded by their due date (target: 100%, zero missed)
- Control-gate exceptions — verification, approval, or dual control skipped (target: zero; these are non-negotiable)
- Wire-instruction changes caught and re-verified (every change verified before funding)
- Cycle time from notice received to staged-for-release (excludes the human control steps)
- Reconciliation of called amount to the commitment ledger completed each call
- Time saved per call (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)
- [Principal Weekly Brief](../skills/principal-weekly-brief/)

## Related Blueprints

This playbook composes skills directly rather than through a single blueprint. For the layered design it sits within, see the [Reference Architecture](../docs/reference-architecture.md).

## Related Case Studies

- [Capital Call Processing](../case-studies/capital-call-processing.md)

## Related Governance Documents

- [Threat Model](../docs/threat-model.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — each call handled from scratch under deadline, banking details re-keyed by hand, one person doing everything.
2. **Controlled** — an authorized-signer matrix with approval thresholds, segregation of duties (preparer ≠ approver ≠ releaser), dual control configured at the bank, and out-of-band wire verification become standing policy. These controls matter regardless of AI and are the heart of the process.
3. **Tracked** — a commitment ledger (unfunded balance, called-to-date, recallable distributions) and pre-verified beneficiary templates for repeat fund wires shrink the fraud surface; the weekly brief surfaces every open call.
4. **AI-assisted** — Document Digest makes notices legible and the action extractor builds the checklist; approved, read-only retrieval of the commitment record can pre-populate the obligation summary — a governed data-access change, not new authority. See [connectors-and-context.md](../docs/connectors-and-context.md).

No stage moves the wire-verification, approval, or dual-control release gates off a human. The separation between making the call legible and touching the money is the whole point.

---

*This playbook is an illustrative operating pattern, not legal, tax, or accounting advice, and not a live integration. It does not approve payments, initiate wires, or move money — those remain human actions under the office's controls. Every output described is an unverified draft requiring human review.*
