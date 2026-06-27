# Case Study: Investment Opportunity Review

How a family office gives an inbound private opportunity a fast, structured first-pass read — to decide whether it is worth more time — without recommending, ranking, or allocating.

> **Fictionalized and illustrative.** This is a sanitized, generalized example. It does not describe any actual family office, employer, client, principal, investment, manager, or document. All names, scenarios, and figures are invented and directional. **Nothing here is a recommendation to invest, an opinion on any opportunity, or investment, legal, tax, or accounting advice.**

---

## Scenario

A family office receives an unsolicited private investment opportunity — a deck excerpt and a founder's email describing a raise. The principal will ask, "Is this worth a closer look?" The office needs a consistent first-pass read that separates what the promoter is claiming from what has actually been verified, and that lists the questions a real diligence process would have to answer — before anyone spends hours on it.

## Operating problem

Inbound deal flow is uneven in quality and arrives faster than a lean team can properly evaluate. The risk runs both ways: a promising opportunity gets a thin, inconsistent look because no one had time, or a weak one consumes diligence hours it never deserved. Screening is structure-heavy and repetitive, but the stakes make sloppiness costly. The office needs triage that is consistent and conservative — and that never drifts into deciding.

## Traditional workflow

An analyst reads the materials, types notes into whatever format they used last time, tries to recall what questions matter for this asset type, and writes a short summary for the principal. Format and rigor vary by analyst and by how busy the week is. The promoter's framing often survives into the summary unchallenged, and the specific diligence questions are reconstructed from memory each time.

## AI-assisted workflow

The operator runs the [Investment Opportunity Review System](../blueprints/investment-opportunity-review-system.md) blueprint:

1. Run **[Investment Memo Screener](../skills/investment-memo-screener/)** on the deck excerpt and founder email to produce a first-pass memo that separates the promoter's thesis from verified fact, lists specific diligence questions, and flags missing financials and terms — making **no recommendation to invest**.
2. If the opportunity is a fund or external manager, run **[Manager Diligence Summarizer](../skills/manager-diligence-summarizer/)** to standardize the manager write-up into a diligence-ready format.
3. If a call with the promoter follows, run **[Meeting Prep Pack](../skills/meeting-prep-pack/)** to build a focused prep brief around the open questions.
4. After the call, run **[Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)** to capture answers, owners, and the next diligence steps.

The AI structures the read and surfaces questions. It does not score the deal, rank it against others, or suggest sizing.

## Inputs

- A deal summary, deck excerpt, CIM excerpt, or founder email (fictional or approved, non-confidential)
- For a fund or manager: fund overview, strategy summary, and manager background, as available
- The office's standard screening questions, if any
- Notes from any introductory call

## Skills used

- [Investment Memo Screener](../skills/investment-memo-screener/) — the first-pass memo
- [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/) — used only if the opportunity is a fund or external manager
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — prep for a promoter or manager call
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — capturing next diligence steps

## Context sources

Manual input first: the operator pastes the materials. Approved, read-only retrieval of an already-received document may reduce copy-and-paste once trusted. No external market data, comparables, or pricing is introduced by the AI. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Review gates

- **Inputs gate:** confirm the materials are appropriate to process and contain no unapproved confidential information.
- **Fact-vs-claim gate:** a competent person confirms that promoter claims are labeled as claims, not facts, and that the memo makes no recommendation.
- **Pre-circulation gate:** the reviewer verifies the summary against source and frames the "worth more time?" question for the principal — the office, not the AI, makes that call.

## Outputs

- A first-pass screening memo (draft) that makes no recommendation
- A standardized manager summary (draft), if applicable
- A diligence question list (draft)
- A meeting prep brief and post-meeting action list (drafts), if a call occurs

## Measurement

How this workflow could be measured ([measurement framework](../docs/measurement-framework.md); figures are directional, not audited):

- **Time saved** — screening time avoided per opportunity.
- **Cycle time reduced** — from "materials received" to "first-pass read ready for the principal."
- **Review exceptions** — memos used without the required review (driven toward zero).
- **Follow-ups captured** — diligence questions and next steps recorded rather than lost.
- **Decisions supported** — "look closer / pass for now" triage decisions the principal made (decisions the office owns, not the AI).
- **Documents summarized** — decks, emails, and manager materials read into a consistent format.
- **Action items created** — owned diligence steps produced.

## Risks and controls

- **Confidentiality** — deal materials are sensitive; use only approved environments and never paste confidential materials into public tools. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Stale information** — figures in a deck may be dated; the reviewer treats all numbers as unverified until confirmed against source.
- **Hallucination** — the AI may fill gaps with plausible but invented financials or terms; every figure is verified, and missing items are flagged, not guessed.
- **Professional advice boundary** — the memo is a structured read, **not** investment advice and **not** a recommendation to invest; it does not opine on suitability, sizing, or allocation.
- **Overreliance** — a polished memo can feel like a verdict; the reviewer keeps it as triage input, and the investment decision stays with people and qualified advisers.

## What remains human

- The decision to invest, pass, or look closer — and all sizing and allocation.
- Verifying every claim, figure, and term against source.
- Real diligence, judgment, and risk assessment.
- The relationship with the promoter or manager.
- Any communication of interest or terms.

## Takeaway

A screener earns its keep by triaging consistently and refusing to decide: it separates claim from fact and lists the right questions fast, so scarce diligence time goes to the opportunities that deserve it — while every judgment about whether and how much to invest stays firmly with people.

---

*This case study is an illustrative operating pattern, not investment, legal, tax, or accounting advice, and not a recommendation regarding any investment. It does not rank opportunities or allocate capital. Every output described is an unverified draft requiring human review.*
