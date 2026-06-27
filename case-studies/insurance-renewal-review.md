# Case Study: Insurance Renewal Review

How a family office reads an insurance renewal for changes, coverage questions, and follow-ups before the broker call — framing everything as questions, never as insurance advice.

> **Fictionalized and illustrative.** This is a sanitized, generalized example. It does not describe any actual family office, employer, client, principal, broker, carrier, policy, or document. All names, scenarios, and figures are invented and directional. **Nothing here is insurance, legal, tax, or risk advice. Coverage questions belong with a licensed broker and counsel.**

---

## Scenario

A family office receives a renewal package from its insurance broker — a renewal proposal and a declarations page for a policy that covers the family's property and liability. Premiums, limits, and a few endorsements appear to have changed from last year. Before the renewal call, the operator wants a clear read of what changed, what questions to ask, and where coverage might have gaps — so the broker conversation is productive rather than a first read of the document in real time.

## Operating problem

Insurance renewals arrive as dense, inconsistent documents, often once a year, so no one builds fluency in reading them. Changes are buried, year-over-year differences are not laid out, and the office is not in a position to give itself insurance advice — that is the broker's and counsel's role. The difficulty is preparing well enough to ask the right questions without overstepping into coverage conclusions the office is not qualified to make.

## Traditional workflow

The operator skims the renewal, compares it as best they can against last year's binder, jots a few questions, and gets on the call — frequently discovering mid-call that a limit or endorsement changed in a way they had not flagged. Important questions surface only after the call, requiring a second round. The read is shallow because the document is hard and the cadence is rare.

## AI-assisted workflow

The operator uses the [Vendor Management System](../blueprints/vendor-management-system.md) pattern, treating the broker relationship and renewal as a vendor review supported by document digestion:

1. Run **[Document Digest](../skills/document-digest/)** on the renewal proposal and declarations page to produce a plain-English summary, the key dates and obligations, changed or unusual terms flagged for review, and the precise questions to put to the broker and counsel — **without giving insurance or legal advice**.
2. Run **[Vendor Review](../skills/vendor-review/)** treating the broker as the service provider: structure the relationship, the renewal terms, apparent cost changes, open service issues, and the questions to resolve before any decision.
3. Run **[Meeting Prep Pack](../skills/meeting-prep-pack/)** to build a focused brief for the renewal call around the open questions and apparent changes.
4. After the call, run **[Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)** to capture the broker's answers, owners, and follow-ups (e.g., obtaining a quote for a higher limit, confirming an endorsement).

Every coverage observation is framed as a question for the broker or counsel — never as a conclusion about what is or is not covered.

## Inputs

- A renewal proposal and declarations page (fictional or approved, non-confidential)
- The prior-year summary or binder, for comparison, as available
- Known changes in the family's circumstances relevant to coverage (e.g., a new asset to schedule)
- Any open service issues with the broker

## Skills used

- [Vendor Review](../skills/vendor-review/) — the broker relationship and renewal review
- [Document Digest](../skills/document-digest/) — the plain-English read of the renewal and questions for broker/counsel
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — prep for the renewal call
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — capturing follow-ups after the call

## Context sources

Manual input first: the operator pastes the renewal text and last year's summary. Approved, read-only retrieval of an already-received renewal document may reduce copy-and-paste once trusted. The AI introduces no outside policy terms, market pricing, or coverage standards. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Review gates

- **Inputs gate:** confirm the documents are appropriate to process and contain no unapproved confidential information.
- **Framing gate:** a competent person confirms that every coverage observation is phrased as a question for the broker or counsel, not as an assertion about coverage.
- **Pre-call gate:** the reviewer verifies the summarized changes against the actual documents before relying on them in the call.

## Outputs

- A plain-English digest of the renewal (draft)
- A list of apparent changes versus the prior year (draft, for verification)
- A question list for the broker and counsel (draft)
- A renewal-call prep brief and post-call action list (drafts)

## Measurement

How this workflow could be measured ([measurement framework](../docs/measurement-framework.md); figures are directional, not audited):

- **Time saved** — review and prep time avoided per renewal.
- **Cycle time reduced** — from "renewal received" to "ready for the broker call."
- **Review exceptions** — digests used without the required verification (driven toward zero).
- **Follow-ups captured** — questions and post-call actions recorded rather than lost.
- **Decisions supported** — renewal decisions the office made with the broker (decisions the office owns, informed by licensed advice).
- **Documents summarized** — renewal proposals and dec pages read into plain English.
- **Action items created** — owned follow-ups produced (quotes to request, endorsements to confirm).

## Risks and controls

- **Confidentiality** — policy documents contain sensitive asset and personal detail; use only approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Stale information** — prior-year comparisons can be wrong if the binder is outdated; the reviewer confirms changes against the current documents.
- **Hallucination** — the AI may misstate a limit, endorsement, or exclusion; every coverage detail is verified against source before the call.
- **Professional advice boundary** — outputs are **questions for a licensed broker and counsel**, not insurance advice and not a coverage opinion. The office does not determine adequacy of coverage itself.
- **Overreliance** — a confident digest can read like a coverage analysis; the reviewer treats it as preparation, and the broker and counsel remain the authority on coverage.

## What remains human

- All coverage judgments and decisions — made with the licensed broker and counsel.
- Verifying every limit, endorsement, and exclusion against the policy.
- Deciding what to bind, change, or decline.
- The relationship with the broker and carrier.
- Any instruction to the broker.

## Takeaway

The win is a well-prepared broker call, not a coverage opinion: the AI lays out what changed and what to ask, so the office walks in informed — while the actual coverage judgment stays where it belongs, with the licensed broker and counsel.

---

*This case study is an illustrative operating pattern, not insurance, legal, tax, or risk advice, and not a coverage opinion. All coverage questions belong with a licensed broker and counsel. Every output described is an unverified draft requiring human review.*
