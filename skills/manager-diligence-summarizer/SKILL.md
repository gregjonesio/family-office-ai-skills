---
name: manager-diligence-summarizer
description: Use this skill to summarize investment manager or fund materials (pitch books, DDQs, factsheets, call notes) into a consistent, diligence-ready format. Produces a structured summary covering strategy, team, track record, fees and liquidity, portfolio construction, risk factors, key questions, and follow-up diligence items. This is a diligence summary, not a recommendation.
---

# Manager Diligence Summarizer

## Purpose

This skill distills investment manager and fund materials into a consistent, diligence-ready summary. It takes pitch books, due-diligence questionnaires, factsheets, and call notes and organizes them into a standard format an allocator can review, compare across managers, and use to drive the next stage of diligence. It produces a structured summary for human review, not a recommendation to allocate.

## When to use this

- Standardizing manager write-ups across an allocation pipeline so they are comparable.
- Preparing a diligence summary for an investment committee or principal.
- Distilling a long pitch book or DDQ into a reviewable one-pager.
- Building a consistent record of how each manager was assessed.

## Inputs

Provide whatever you have; the skill works with partial material and flags gaps.

- **Source material:** pitch book, DDQ, factsheet, presentation, term summary, or call notes.
- **Strategy descriptor** if known (e.g., long/short equity, private credit, venture, real assets).
- **Any specific concerns** you want the summary to probe.

## Output

Produce a summary with these sections, in this order:

1. **Strategy overview** — what the manager does, markets, instruments, and stated edge.
2. **Team** — key people, backgrounds (as stated), and key-person dependencies.
3. **Track record summary** — stated figures with periods and caveats.
4. **Fees and liquidity** — fees, hurdle/high-water mark, lock-up, redemption terms, gates.
5. **Portfolio construction** — concentration, sizing, leverage, exposures.
6. **Risk factors** — material risks as described and as inferred.
7. **Key questions** — the questions to put to the manager.
8. **Follow-up diligence items** — documents and confirmations to obtain.

Use the [manager diligence template](../../templates/manager-diligence-template.md) as the output structure.

## Instructions

- Draw only from the provided material. Do not add performance figures, AUM, or claims not present.
- Treat all **track record and fee figures as unverified.** Note the period, whether returns are net of fees, and any methodology caveats. Flag selective or composite periods.
- Separate **stated information** from **assumptions.** Mark inferred items *(assumption)*.
- Identify **key-person risk** and any dependency the materials reveal.
- Make *Key questions* specific to this manager and strategy, tied to what is in (or missing from) the material.
- Keep the summary neutral. Do not opine on whether to allocate.

## Quality control

- **Missing information:** Manager materials are promotional and selective. Actively list what a competent allocator would require that was not provided (audited statements, full track record, ADV/registration, references, DDQ, terms).
- **Hallucination risk:** Do not supply returns, AUM, Sharpe ratios, or other figures not in the source. If a figure is absent, mark it *(missing)*.
- **Confidentiality:** Treat the material as confidential; introduce no outside information about the manager or its principals.
- **Uncertainty:** Where claims are vague or unsupported (e.g., "consistent outperformance"), convert them into key questions rather than restating them as fact.

## Do not

- Do not recommend allocating to, or avoiding, the manager.
- Do not provide investment, legal, tax, or valuation advice.
- Do not invent or estimate track record, AUM, or fee figures.
- Do not present marketing claims as verified performance.
- Do not commit the office to any allocation or action.
- Do not omit the *Follow-up diligence items* section.

## Example request

> "Using the manager-diligence-summarizer skill, summarize this manager's materials into a diligence-ready format: [paste pitch book notes / DDQ excerpts / call notes]. Strategy is long/short equity."

---

*This skill supports human diligence and produces an unverified summary of promotional material for review. It does not provide investment, legal, tax, accounting, or compliance advice, makes no recommendation to allocate or avoid, and does not authorize any decision, transaction, or communication. A competent person must independently verify all figures before they are used.*
