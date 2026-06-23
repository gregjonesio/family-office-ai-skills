# Blueprint: Vendor Management System

A composed system for reviewing vendor proposals and renewals, digesting the underlying documents, preparing for negotiation, and tracking follow-through — without approving, terminating, signing, or sending anything. This is a **design pattern**, not an automation. Read-only, human-in-the-loop, non-advisory. Contractual questions go to counsel.

---

## Purpose

Give an operator a consistent, reviewable way to evaluate a vendor relationship: a structured review, a plain-English read of the documents, prepared negotiation questions, and a tracked action list — all as drafts for a human decision.

## When to use

- A vendor or service-provider renewal or proposal needs review.
- A service issue or performance concern needs to be documented and escalated.
- Preparing for a vendor negotiation or relationship-review meeting.

## Inputs

- Vendor proposal, renewal notice, or invoice
- Contract or contract excerpt
- Service notes and performance history
- Meeting notes from vendor discussions

## Context sources

Manual input first; approved read-only connectors where appropriate. Possible sources: proposals, renewal notices, service notes, contracts, and meeting notes. Contracts are sensitive; provide high-risk documents manually after review. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Skills used

- [Vendor Review](../skills/vendor-review/) — the structured review
- [Document Digest](../skills/document-digest/) — plain-English read of contracts/notices
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — negotiation/relationship-review prep
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — follow-ups after the discussion

## Workflow sequence

1. Run **Document Digest** on the proposal/renewal/contract → plain-English summary, key dates, obligations, unusual terms, and questions for counsel.
2. Run **Vendor Review** → terms, service issues, cost considerations, risks, vendor questions, and a recommended process next step.
3. Run **Meeting Prep Pack** for the vendor discussion → questions and desired outcomes.
4. After the discussion, run **Post-Meeting Action Extractor** → action list and escalation items.
5. **Human review gate** → verify terms against the actual documents; route contract questions to counsel.

## Human review gates

- **Gate 1 — Documents:** verify the digest against the source document; do not act on an unreviewed summary.
- **Gate 2 — Review:** confirm the vendor review's terms and figures; confirm it makes no fairness or legal determination.
- **Gate 3 — Decision:** a person decides whether to renew, renegotiate, escalate, or replace; counsel handles contractual questions.

## Outputs

- Vendor review memo
- Renewal questions
- Negotiation prep
- Action list
- Escalation summary

## Measurement metrics

- Vendor reviews completed before renewal deadlines
- Human-review completion rate (target: 100%)
- Renewals reviewed vs. auto-renewed unintentionally (target: zero unintentional)
- Estimated time saved (directional)

See [measurement-framework.md](../docs/measurement-framework.md). Value figures are directional only.

## Failure modes

- Relying on an unreviewed contract summary
- Asserting a price is fair or unfair without a basis
- Drifting into legal conclusions about contract terms
- Missing an auto-renewal notice deadline
- Acting on retrieval (e.g., treating a draft as an instruction to proceed)

## Prohibited actions

- Do not terminate vendors.
- Do not approve contracts.
- Do not provide legal advice.
- Do not send negotiation emails automatically.
- Do not rely on unreviewed contract summaries.
- No investment, tax, or fiduciary advice.

## Implementation notes

Provide contracts manually after a person has reviewed them. Treat the digest's "questions for counsel" as a routing step, not a substitute for counsel. Watch renewal/notice deadlines closely — the system surfaces them but does not act on them.

---

*This blueprint is an operational design pattern, not legal, procurement, tax, or fiduciary advice, and not a live integration. It does not approve, sign, renew, or terminate anything. Every output is an unverified draft requiring human review; route contractual questions to counsel.*
