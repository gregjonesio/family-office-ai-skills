# Playbook: Investment Opportunity Intake

How a family office triages inbound investment opportunities through a single front door and against its investment policy — separating the promoter's thesis from verified fact, checking fit and pacing before diligence time is spent, and routing decisions to a governed investment committee. AI screens; people decide, and the screen recommends nothing. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, opportunity, manager, or deal. Nothing here is investment, legal, or tax advice, ranks no opportunity, and recommends no allocation. Every AI output described is an unverified draft requiring human review.

---

## Objective

Give every inbound opportunity a fast, consistent first-pass read through one intake channel, tested against the office's investment policy statement (IPS) and commitment pacing, so real diligence time is spent only where the opportunity fits the mandate — with promoter claims separated from fact, conflicts surfaced, and the advance/decline decision owned by a governed investment committee rather than made socially.

## Operating Problem

Deal flow arrives constantly and in inconsistent forms — cold founder emails, decks, CIM excerpts, manager pitch books, and warm introductions — and a lean investment function cannot run full diligence on each. Two failure modes dominate. First, **the bypassed gate**: a principal hears a pitch at a dinner and effectively commits before any diligence, and the office is left papering a decision already made. Second, **the halo effect**: a warm introduction or a polished deck pulls attention and capital out of proportion to merit. Underneath both is a discipline problem — without a single front door, an IPS to test fit, and a pacing model to manage how much is committed in any vintage, the portfolio drifts past its own concentration and liquidity limits one attractive deal at a time.

## Typical Trigger

An opportunity arrives — an inbound email, an introduction, a deck, or a manager's materials — or a periodic pipeline review surfaces items awaiting a first read. In a disciplined office, *every* opportunity, including the principal's own sourced deals, enters through the same intake.

## Frequency

Continuous intake with a periodic (often weekly) triage to clear the queue, feeding a regular investment committee cadence.

## Primary Stakeholders

- **CIO / investment lead (owner)** — runs the screen, applies the IPS, and prepares items for the committee.
- **Investment committee** — the governed decision body: quorum, disclosed conflicts, a vote, and minutes, even in a single-family office.
- **Principal / family** — set the mandate via the IPS and make or ratify allocation decisions; subject to the same gate as any other source.
- **Operations / EA** — schedule introductory calls only for items the screen advances.

## Required Inputs

- The opportunity materials: deal summary, deck notes, CIM excerpt, founder email, or call notes
- For managers and funds: pitch book, DDQ, factsheet, references, track-record detail
- The IPS: mandate, target allocation, concentration and liquidity limits (as context, not a score the AI computes)
- The commitment pacing model and current vintage exposure
- Any conflict or related-party disclosure (e.g., the family co-investing alongside the GP)

Treat all track-record, return, and fee figures as unverified. Handle material non-public information per policy and keep it out of unapproved tools.

## AI-Assisted Activities

- Convert a deal summary, deck, CIM excerpt, or founder email into a structured first-pass memo with [Investment Memo Screener](../skills/investment-memo-screener/) — separating the promoter's thesis from verified fact and listing specific diligence questions and missing items.
- Summarize manager and fund materials into a diligence-ready format with [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/), treating all figures as unverified.
- For advanced items, draft an introductory-call brief with [Meeting Prep Pack](../skills/meeting-prep-pack/) and capture follow-ups with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

AI structures and surfaces questions. It applies no IPS score, makes no recommendation to invest, pass, or size, and ranks nothing.

## Human Responsibilities

- Route every opportunity through the single front door, including socially sourced deals.
- Test fit against the IPS — mandate, concentration, liquidity — and against pacing; this judgment is human.
- Verify every figure and claim against source before relying on it; run references independently.
- Surface and manage conflicts: disclosure and, where needed, recusal from the committee vote.
- Decide what advances and what is declined, through the committee, and own all communication with founders and managers.

## Review Gates

1. **Intake gate (single front door)** — confirm the opportunity entered through the standard channel and that materials are free of mishandled MNPI or unapproved confidential data. The gate exists precisely to catch the deal that tried to skip it.
2. **Fact-vs-claim gate** — a competent person confirms the screen has separated promoter claims from verified fact and has not adopted figures as true.
3. **Policy-and-pacing gate** — a person tests the opportunity against the IPS and the pacing model before it consumes diligence resources.
4. **Committee gate (governed decision)** — the investment committee decides under quorum, with conflicts disclosed and the decision recorded in minutes; the screen makes no recommendation and assigns no rank.

## Outputs

- A structured first-pass screening memo (draft)
- A diligence-ready manager summary, where relevant (draft)
- A list of specific diligence questions and missing items (draft)
- Introductory-call prep and follow-ups for advanced items (draft)

## Risks

- **Overreliance on a polished screen** — a clean memo can lend unearned credibility; it remains a triage draft, not diligence.
- **Adopted claims** — the AI may restate a promoter's figure as fact; the fact-vs-claim gate catches it.
- **Hallucination** — invented metrics or terms; verified against source.
- **Advice boundary** — the screen produces no recommendation, rank, or sizing; those are committee decisions.
- **Confidentiality and MNPI** — handle per policy; see [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **The bypassed gate.** The principal commits socially and diligence becomes a formality. *Control:* a single front door and a standing rule that all opportunities — including the principal's — go through the same intake and committee before capital is committed.
- **Halo effect.** A warm intro or strong brand substitutes for analysis. *Control:* the fact-vs-claim discipline and a written diligence checklist applied uniformly regardless of source.
- **No pacing discipline.** The office over-commits in one vintage and is starved of dry powder in the next, magnifying the denominator effect in down markets. *Control:* a commitment pacing model reviewed at the policy-and-pacing gate.
- **Concentration drift.** Successive attractive deals push a sector or manager past IPS limits without anyone deciding to. *Control:* concentration and liquidity limits in the IPS, checked at intake.
- **Undisclosed conflicts.** The family co-invests alongside a GP, or a related party benefits, without disclosure or recusal. *Control:* a conflicts register and recusal at the committee gate.
- **Decision with no record.** An allocation is made informally with no minutes, leaving no rationale of record. *Control:* committee minutes capturing the decision and its basis.

## Metrics

- Opportunities triaged within the cadence (target: queue cleared each cycle)
- Share of opportunities entering through the single front door (target: 100%)
- Review-gate completion rate, including committee minutes (target: 100%)
- Diligence time avoided on items declined at screen (directional)
- Vintage exposure kept within the pacing model and IPS limits

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Investment Memo Screener](../skills/investment-memo-screener/)
- [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/)
- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Investment Opportunity Review System](../blueprints/investment-opportunity-review-system.md)

## Related Case Studies

- [Investment Opportunity Review](../case-studies/investment-opportunity-review.md)

## Related Governance Documents

- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Measurement Framework](../docs/measurement-framework.md)
- [Evaluation and Red-Team Guide](../docs/evaluation-guide.md) and the [Investment Memo Screener evals](../evals/investment-memo-screener-evals.md)

## Evolution Path

1. **Ad hoc** — deals arrive through many channels, get evaluated unevenly, and the principal sometimes commits before diligence.
2. **Governed** — an IPS defines the mandate and limits, a single front door routes all intake, and an investment committee with quorum, conflict disclosure, and minutes owns decisions. These governance controls stand independent of AI.
3. **Paced** — a commitment pacing model manages vintage diversification and liquidity, checked before diligence resources are spent.
4. **AI-assisted** — the screener and diligence summarizer produce consistent first-pass reads, and approved, read-only retrieval of prior screens on the same manager gives reviewers context — a governed data-access change, not new authority.

No stage lets the screen recommend, rank, or size, or lets a deal skip the committee. The advance/decline decision stays human and governed.

---

*This playbook is an illustrative operating pattern, not investment, legal, or tax advice, and not a live integration. It recommends no allocation and ranks no opportunity. Every output described is an unverified draft requiring human review.*
