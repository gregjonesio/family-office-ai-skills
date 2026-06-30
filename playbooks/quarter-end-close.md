# Playbook: Quarter-End Close

How a family office runs a controlled, on-time close across a multi-entity structure — working a day-by-day close calendar, reconciling every account, handling investment NAV lag and intercompany eliminations, and producing a consistent family reporting package — under a preparer/reviewer separation, while the accounting judgment and sign-off stay with the controller and CFO. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, entity, ledger, statement, or account. Nothing here is accounting, tax, audit, or financial advice, performs no reconciliation, and books no entry. Every AI output described is an unverified draft requiring human review.

---

## Objective

Close the books and produce reporting on a reliable cadence: a day-by-day checklist worked to completion, every account reconciled, intercompany balances eliminated, investment values brought in correctly despite reporting lag, and a consolidated family package that trends cleanly quarter to quarter — with the controller and CFO owning every figure and the sign-off, and a second set of eyes on the work.

## Operating Problem

A family office closes across a web of entities — investment LPs and LLCs, operating companies, trusts, and personal accounts — each with its own statements, capital activity, and supporting documents that consolidate into one family picture. The close is a coordination problem under a hard deadline, with three recurring difficulties. **NAV lag**: fund and partnership values arrive on a delay (capital statements and K-1s often lag a quarter or more), so the office estimates and then trues up — and mishandling this restates performance every period. **Intercompany**: loans and shared expenses between entities must be eliminated to avoid double-counting. **Thin segregation of duties**: a one- or two-person accounting shop struggles to separate the preparer from the reviewer, which is exactly where errors and fraud hide. The discipline a mature office imposes is a documented close calendar, a standing reconciliation set, a true-up convention for lagged values, and an independent review — often an outside CPA where internal staff is too lean to self-check.

## Typical Trigger

The period-end date and the office's close calendar, plus the arrival of the quarter's custodial, bank, and fund statements, capital-activity notices, and supporting documents.

## Frequency

Quarterly, with a monthly variant in many offices and a heavier annual close that feeds tax and the audit or review.

## Primary Stakeholders

- **Controller (owner, preparer)** — runs the close calendar, performs reconciliations, and prepares reporting.
- **CFO (reviewer)** — reviews against reconciled records and owns the reporting and the sign-off.
- **Accounting staff / bookkeeper** — execute ledger work; in lean shops this overlaps with the controller, raising the need for outside review.
- **Outside CPA** — provides the independent review where internal segregation of duties is limited.
- **Auditor and tax advisors** — downstream consumers; the office's work supports, never replaces, theirs.

## Required Inputs

- The close calendar and prior-period working papers
- Custodial, bank, and fund/partnership statements for the period
- Capital-activity notices (calls, distributions) and supporting documents
- Invoices, expense records, intercompany activity, and loan balances
- The chart of accounts, entity structure, and ownership/consolidation map
- Prior-quarter estimates awaiting true-up

Statements and account detail are highly sensitive; provide them manually in approved environments only.

## AI-Assisted Activities

- Produce plain-English reads of statements, capital-activity notices, and supporting documents with [Document Digest](../skills/document-digest/): amounts, dates, obligations, and questions for review — **without performing accounting or rendering advice**.
- Turn the close calendar and open items into an owned, tracked list with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) (used as a checklist-to-action extractor): owners, deadlines, and dependencies for each close task, including statements still outstanding and estimates awaiting true-up.
- Surface close status, the deadline, and open items in the [Principal Weekly Brief](../skills/principal-weekly-brief/) until the close is signed off.

AI reads, organizes, and reminds. It performs no reconciliation, books no entry, computes no balance as authoritative, eliminates no intercompany item, and renders no accounting or tax judgment.

## Human Responsibilities

- Work the close calendar and perform all reconciliations and ledger work.
- Verify every figure against source statements; nothing the AI restates is trusted as a number.
- Apply the true-up convention for lagged investment values and eliminate intercompany balances.
- Apply all accounting and tax judgment, and own the reporting and the close sign-off.
- Ensure a reviewer independent of the preparer checks the work — internally, or via outside CPA where staff is too lean.

## Review Gates

1. **Inputs gate** — confirm statements and documents are complete, current, and appropriate to process, and chase what is outstanding before the close proceeds.
2. **Reconciliation gate** — a competent person reconciles every account — bank, custodian, intercompany, and loan balances; the AI's digests are inputs to that work, never the reconciliation itself.
3. **Preparer/reviewer gate (segregation of duties)** — a reviewer independent of the preparer checks reconciliations and entries; where internal separation is not possible, an outside CPA provides it.
4. **Reporting-review gate** — the CFO reviews the consolidated package against reconciled records, confirming consistency with prior periods, before it is shared.
5. **Sign-off gate** — a person signs off the close; the AI never closes a period.

## Outputs

- Plain-English digests of statements and supporting documents (draft)
- An owned, tracked close checklist with status and outstanding-item list (draft)
- A close-status entry in the weekly brief (draft)
- A question list for review, audit, or tax (draft)

## Risks

- **Misread figure** — the AI may misstate an amount; every number is verified against source and reconciled by a person.
- **Dropped reconciling item** — an open item lost is a close error; the tracked checklist and reconciliation gate guard against it.
- **Overreliance** — a tidy checklist can imply the work is done; reconciliations, review, and sign-off remain human.
- **Advice and authority boundary** — outputs are summaries and checklists, not accounting, tax, or audit work; the close is owned by the controller and CFO.
- **Confidentiality** — financial detail is highly sensitive; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **NAV lag mishandled.** Lagged fund values are booked as final and then restated, so performance moves every quarter. *Control:* a documented estimate-then-true-up convention and a tracked list of estimates awaiting true-up.
- **No segregation of duties.** A single person prepares and reviews the close, where errors and fraud hide. *Control:* a preparer/reviewer separation, backstopped by an outside CPA review when staff is too lean to self-check.
- **Intercompany out of balance.** Loans and shared costs between entities are not eliminated, double-counting the family picture. *Control:* a standing intercompany reconciliation in the close calendar.
- **Estimates never trued up.** A placeholder figure persists for quarters because nothing tracks it back. *Control:* an open-estimates log carried period to period.
- **Late inputs stall the close.** Statements or K-1s arrive late and there is no chase process, so the deadline slips. *Control:* an outstanding-items list and a standing chase as a calendar task.
- **Inconsistent reporting package.** The family package changes shape each quarter, so nothing can be trended. *Control:* a fixed reporting template reviewed for prior-period consistency.

## Metrics

- Close completed by the deadline (target: every period)
- Reconciliation, independent-review, and sign-off gate completion (target: 100%)
- Estimates trued up within the agreed window
- Intercompany balances eliminated to zero each period
- Open checklist items carried to closure vs. dropped
- Coordination and document-reading time saved (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)
- [Principal Weekly Brief](../skills/principal-weekly-brief/)

## Related Blueprints

This playbook composes skills directly rather than through a single blueprint. For the layered design it sits within, see the [Reference Architecture](../docs/reference-architecture.md).

## Related Case Studies

- [Capital Call Processing](../case-studies/capital-call-processing.md) — capital activity that feeds the close.

## Related Governance Documents

- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Operating Model](../docs/operating-model.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — the close is run from memory each period, inputs chased reactively, and one person both prepares and checks the work.
2. **Calendared and reconciled** — a documented day-by-day close calendar, a standing reconciliation set, and a true-up convention for lagged values bring the close under control. These disciplines stand independent of AI.
3. **Independently reviewed** — a preparer/reviewer separation, backstopped by an outside CPA where staff is lean, and a fixed, trendable reporting package raise reliability.
4. **AI-assisted** — Document Digest makes statements legible and the action extractor builds and tracks the checklist; approved, read-only retrieval of prior working papers can seed the close — a governed data-access change, not new authority.

No stage lets the AI reconcile, book entries, eliminate intercompany items, or sign off a close. The accounting work, the independent review, and the sign-off stay human.

---

*This playbook is an illustrative operating pattern, not accounting, tax, audit, or financial advice, and not a live integration. It performs no reconciliation, books no entry, and closes no period. Every output described is an unverified draft requiring human review.*
