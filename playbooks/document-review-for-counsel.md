# Playbook: Document Review for Counsel

How a family office prepares documents for legal review — triaging what the office can handle against what must go to counsel, making documents legible, extracting key dates and obligations into the contract calendar, and routing the right questions through privileged channels — so legal time is spent on judgment, not first-pass reading. The office triages and routes; counsel interprets and advises. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, document, agreement, or matter. Nothing here is legal advice, interprets no document as a professional, and substitutes for no legal review. Every AI output described is an unverified draft requiring human review.

---

## Objective

Hand counsel a clean, well-framed package: a plain-English read of the document, the key dates and obligations extracted, unusual terms flagged, and a precise list of questions — routed through the right channel and with privilege protected — so legal review starts from an organized brief, routine matters are handled efficiently, and both the office's and counsel's time are used well, with interpretation left to counsel.

## Operating Problem

Documents needing legal review arrive constantly — agreements, subscription documents, notices, amendments, and correspondence — and most carry routine terms with a few that genuinely need counsel. A lean office faces a triage dilemma: send everything to counsel and costs balloon with no scoping; read first and route nothing and real risk slips through. Two further hazards sit underneath. **Privilege**: legal material run through an unapproved tool or shared with the wrong recipients can waive the protection that makes candid legal advice possible — a real operational risk when summarizing documents with AI. **Authority**: signing outside a delegation-of-authority schedule binds the family without the right approval. And key dates — renewal windows, options, termination rights — buried in executed agreements are missed if no one extracts them. The discipline a mature office imposes is a written triage taxonomy, privileged-channel handling, a delegation-of-authority schedule, key-date extraction into a contract calendar, and managed outside-counsel relationships with budgets.

## Typical Trigger

A document arrives or is identified that needs legal review — an agreement to sign, a notice to act on, an amendment to assess, or correspondence to answer.

## Frequency

On demand as documents arise, often clustered around transactions, renewals, and entity activity.

## Primary Stakeholders

- **Operations / chief of staff (owner)** — triages, prepares the document for review, extracts key dates, and routes it.
- **Counsel (inside or outside)** — interprets the document, advises, and owns every legal conclusion; manages privilege.
- **Principal / authorized signatory** — decides and signs on counsel's advice within the delegation-of-authority schedule.

## Required Inputs

- The document or excerpt to be reviewed (provided manually after review)
- Related agreements or prior versions for context
- The specific question or decision the document bears on
- The office's triage taxonomy (what goes to counsel vs. what the office handles) and delegation-of-authority schedule
- Outside-counsel panel, billing guidelines, and any matter budget

Documents for legal review are sensitive and often privileged; provide them manually in approved environments, handle privilege carefully, and limit recipients.

## AI-Assisted Activities

- Produce a plain-English read of the document with [Document Digest](../skills/document-digest/): a summary, key dates and obligations, unusual terms flagged for review, and the precise questions to put to counsel — **without giving legal advice or interpreting the document as a professional**.
- Turn the digest's questions, key dates, and required steps into an owned, tracked list with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/): what goes to counsel and by when, which dates feed the contract calendar, and what the office must confirm.

AI makes the document legible and frames questions. It interprets nothing as a professional, recommends no signing or declining, and renders no legal conclusion.

## Human Responsibilities

- Apply the triage taxonomy: decide what goes to counsel and what is routine, on policy.
- Protect privilege — keep legal material in approved, privileged channels and limit recipients.
- Verify the digest against the actual document before relying on it.
- Obtain and rely on counsel's interpretation for any legal question — the digest's questions are a routing aid, not an answer.
- Extract key dates into the contract calendar, and decide and sign only within the delegation-of-authority schedule on counsel's advice.

## Review Gates

1. **Privilege gate** — before any document is summarized or shared, a person confirms it is handled in an approved, privileged channel and routed only to those entitled to see it. Privilege, once waived, is hard to restore.
2. **Triage gate (taxonomy)** — a person confirms which questions and documents go to counsel and which are routine; the AI flags candidates, the office decides on policy.
3. **Document gate** — verify the digest against the source document; do not act on an unreviewed summary.
4. **Interpretation gate** — counsel provides every legal interpretation; the office's digest informs the question, never the answer.
5. **Authority gate** — execution occurs only within the delegation-of-authority schedule, on counsel's advice; key dates and an executed copy are recorded.

## Outputs

- A plain-English digest of the document (draft)
- A flagged list of unusual terms and extracted key dates (draft)
- A precise question list framed for counsel (draft)
- An owned routing-and-follow-up list, including contract-calendar dates (draft)

## Risks

- **Privilege waiver** — summarizing or sharing privileged material through unapproved tools or with the wrong recipients can waive protection; the privilege gate is mandatory.
- **Mistaking triage for advice** — a digest is not legal review; the interpretation gate keeps the boundary clear.
- **Reliance on an unreviewed summary** — the document gate is mandatory before any reliance.
- **Hallucination** — the AI may misread a term, date, or party; all are verified against source.
- **Confidentiality** — legal documents are highly sensitive; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md) and [threat-model.md](../docs/threat-model.md).

## Common Failure Points

- **Privilege waived.** Privileged material is run through an unapproved tool or forwarded to recipients who break the privilege. *Control:* the privilege gate — approved channels and need-to-know distribution before any summarization.
- **Signing outside authority.** A document is executed by someone without authority for that matter or amount, binding the family improperly. *Control:* a delegation-of-authority schedule enforced at the authority gate.
- **Missed key dates.** A renewal, option, or termination right buried in an executed agreement passes because no one extracted it. *Control:* key-date extraction into a contract calendar at intake.
- **Executed copy not stored.** The fully executed agreement is never filed, so the office cannot later prove its terms. *Control:* an execution-copy repository as a closing step.
- **No triage discipline.** Either everything goes to counsel (cost with no scoping) or nothing does (risk). *Control:* a written triage taxonomy and managed outside-counsel budgets.
- **Counsel cost overruns.** Open-ended matters run up fees with no budget or scope. *Control:* matter budgets and billing guidelines with the outside-counsel panel.

## Metrics

- Documents triaged and routed within the office's target time
- Privilege and authority gate completion (target: 100%)
- Key dates extracted into the contract calendar (target: every executed agreement)
- First-pass reading time saved before counsel (directional)
- Questions to counsel framed precisely vs. open-ended
- Outside-counsel spend within matter budgets

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Vendor Management System](../blueprints/vendor-management-system.md) — where document digestion routes contractual questions to counsel.

## Related Case Studies

- [Capital Call Processing](../case-studies/capital-call-processing.md)
- [Insurance Renewal Review](../case-studies/insurance-renewal-review.md)

## Related Governance Documents

- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Threat Model](../docs/threat-model.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Evaluation and Red-Team Guide](../docs/evaluation-guide.md) and the [Document Digest evals](../evals/document-digest-evals.md)

## Evolution Path

1. **Ad hoc** — documents go to counsel inconsistently, key dates live in the agreements themselves, and privilege handling is informal.
2. **Triage discipline** — a written taxonomy of what goes to counsel vs. what the office handles, privileged-channel handling, and a delegation-of-authority schedule control cost, risk, and privilege. These stand independent of AI.
3. **Lifecycle managed** — key-date extraction into a contract calendar, an execution-copy repository, and managed outside-counsel panels with budgets close the loop from intake to storage.
4. **AI-assisted** — Document Digest makes documents legible and frames questions, and the action extractor tracks routing and dates; approved, read-only retrieval of prior versions supports comparison — a governed data-access change, not new authority.

No stage lets the AI interpret a document as a professional, recommend signing or declining, or render a legal conclusion. Interpretation stays with counsel.

---

*This playbook is an illustrative operating pattern, not legal advice, and not a live integration. It interprets no document as a professional and substitutes for no legal review. Every output described is an unverified draft requiring human review; legal interpretation goes to counsel.*
