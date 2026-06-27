# Case Study: Capital Call Processing

How a family office summarizes a capital call notice — obligations, dates, amounts, approvals, the wiring workflow, and recordkeeping steps — without approving payment, initiating a wire, or giving legal or tax advice.

> **Fictionalized and illustrative.** This is a sanitized, generalized example. It does not describe any actual family office, employer, client, principal, fund, document, or account. All names, scenarios, and figures are invented and directional. **Nothing here approves a payment, initiates a wire, or constitutes legal, tax, or accounting advice.**

---

## Scenario

A family office receives a capital call notice from a fund it has committed to. The notice states an amount due, a due date, wiring instructions, and references to the relevant sections of the fund's governing documents. The operator needs to capture the obligation accurately, route it for the required approvals, prepare the payment workflow for a person to execute, and record everything correctly — with no missed date and no detail dropped.

## Operating problem

Capital calls are time-sensitive, infrequent enough that the office never builds routine around them, and unforgiving of error: a missed due date or a misread amount has real consequences, and wiring instructions are a known fraud target. A lean office handles each call somewhat from scratch, under deadline, while the substance — amounts, dates, approvals, recordkeeping — must be exactly right. The difficulty is doing time-critical, detail-heavy processing reliably without ever letting the AI touch the money.

## Traditional workflow

The operator reads the notice, notes the amount and due date, emails whoever approves payments, manually re-keys the wiring details, asks the bank to prepare the wire, and updates the commitment tracker — each step by hand, under time pressure, with the wiring details transcribed manually (the riskiest part). Approval status and recordkeeping live in scattered emails.

## AI-assisted workflow

The operator composes document digestion with briefing and action extraction:

1. Run **[Document Digest](../skills/document-digest/)** on the capital call notice to produce a plain-English summary of the obligation: amount due, due date, the commitment it draws against, any references to the governing documents, and the precise questions to put to fund counsel or the administrator if anything is ambiguous — **without giving legal or tax advice**.
2. Run **[Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)** (used here as an obligation-to-action extractor) to turn the notice into a clean, owned checklist: confirm the amount and date against the notice, obtain the required internal approvals, have a person verify wiring instructions through an independent channel, schedule the payment for a person to execute, and complete recordkeeping.
3. Run **[Principal Weekly Brief](../skills/principal-weekly-brief/)** to surface the pending call, its due date, and its approval status in the weekly view so it is visible until closed.

The AI summarizes, structures, and reminds. It does not approve the payment, transcribe wiring details as if verified, or initiate anything.

## Inputs

- A capital call notice (fictional or approved, non-confidential)
- The commitment record this call draws against, as available
- The office's approval and payment-control policy (who approves, who executes)
- Prior call history for the same commitment, if any

## Skills used

- [Document Digest](../skills/document-digest/) — the plain-English summary of the obligation
- [Principal Weekly Brief](../skills/principal-weekly-brief/) — surfacing the pending call and its due date in the weekly view
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — turning the notice into an owned checklist

## Context sources

Manual input first: the operator pastes the notice. Approved, read-only retrieval of an already-received notice or the commitment record may reduce copy-and-paste once trusted. **Wiring instructions are never treated as verified from the document alone** — a person confirms them through an independent, known channel. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Review gates

- **Inputs gate:** confirm the notice is appropriate to process and contains no unapproved confidential information beyond what is needed.
- **Amount-and-date gate:** a competent person verifies the amount due and due date against the notice and the commitment record.
- **Wire-verification gate:** a person independently verifies wiring instructions through a known channel — never solely from the notice — before any payment is prepared.
- **Approval gate:** the required approver(s) authorize the payment per the office's controls. The AI never approves.
- **Execution gate:** a person initiates the wire. The system never does.

## Outputs

- A plain-English summary of the capital call obligation (draft)
- An owned processing checklist: confirm, approve, verify wire, schedule, record (draft)
- A weekly-brief entry surfacing the pending call and due date (draft)
- A question list for fund counsel or the administrator, if anything is ambiguous (draft)

## Measurement

How this workflow could be measured ([measurement framework](../docs/measurement-framework.md); figures are directional, not audited):

- **Time saved** — processing and summarization time avoided per call.
- **Cycle time reduced** — from "notice received" to "ready for approval," excluding the human control steps.
- **Review exceptions** — instances where a control gate was skipped (target: zero — these gates are non-negotiable).
- **Follow-ups captured** — checklist items and recordkeeping steps tracked to completion.
- **Decisions supported** — approvals routed and recorded (the approval is the approver's, not the AI's).
- **Documents summarized** — capital call notices read into plain English.
- **Action items created** — owned processing and recordkeeping steps produced.

## Risks and controls

- **Confidentiality** — notices contain account and commitment detail; use only approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Stale information** — a remembered amount or date can be wrong; every figure is verified against the current notice and commitment record.
- **Hallucination** — the AI may misread an amount, date, or account reference; all are verified against source, and wiring details are independently confirmed by a person.
- **Fraud and payment-control risk** — wiring instructions are a fraud target; they are verified through an independent known channel and never trusted from the document or the AI alone.
- **Professional advice boundary** — outputs are a summary and a checklist, **not** legal, tax, or accounting advice; ambiguities go to counsel or the administrator.
- **Overreliance** — a clean checklist can create false comfort; the approval, wire verification, and execution gates remain human and mandatory.

## What remains human

- Approving the payment, under the office's controls.
- Independently verifying wiring instructions.
- Initiating the wire — the system never moves money.
- Any legal or tax judgment on the call or the governing documents.
- Final recordkeeping sign-off and the fund relationship.

## Takeaway

AI can make a time-critical obligation legible and trackable — summarizing the call and building the checklist — but the controls that protect the money (approval, independent wire verification, execution) stay human by design, and that separation is the whole point.

---

*This case study is an illustrative operating pattern, not legal, tax, or accounting advice. It does not approve payments, initiate wires, or move money — those remain human actions under the office's controls. Every output described is an unverified draft requiring human review.*
