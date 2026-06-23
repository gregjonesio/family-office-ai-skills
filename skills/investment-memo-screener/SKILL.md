---
name: investment-memo-screener
description: Use this skill to convert a deal summary, pitch deck notes, CIM excerpt, founder email, or other investment opportunity material into a structured first-pass investment memo. Produces a screening memo with an overview, the thesis as presented, key risks, diligence questions, missing information, potential fit, and a suggested next step. This is a screen, not a recommendation.
---

# Investment Memo Screener

## Purpose

This skill converts raw investment opportunity material — a deal summary, pitch deck notes, a CIM excerpt, a founder email — into a consistent, first-pass investment memo. It standardizes the front of the deal-flow funnel so every inbound opportunity receives the same disciplined initial treatment, surfaces the right diligence questions, and flags what is missing. It produces a screening artifact for human review, not an investment recommendation.

## When to use this

- Triaging inbound deal flow into a consistent screening format.
- Turning a founder email or pitch deck into a structured memo before an investment discussion.
- Preparing a first-pass write-up for an investment committee or principal to react to.
- Building a uniform record of how each opportunity was initially assessed.

## Inputs

Provide whatever you have; the skill works with partial material and flags gaps.

- **Source material:** deal summary, pitch deck notes, CIM excerpt, founder email, call notes, or term sheet.
- **Instrument / structure** if known (equity, SAFE, convertible, debt, fund interest, direct, co-invest).
- **Amount and terms** as presented.
- **Any mandate context** you want it screened against (sector, stage, size, liquidity, concentration limits) — kept generic.

## Output

Produce a memo with these sections, in this order:

1. **Company / opportunity overview** — what it is, stage, structure, amount, terms (as stated).
2. **Investment thesis (as presented)** — the case *as the source presents it*, not an endorsement.
3. **Key risks** — table of risks and why each matters.
4. **Diligence questions** — the questions that must be answered before this could advance.
5. **Missing information** — material information not provided.
6. **Potential fit** — neutral mapping to a generic mandate (sector, stage, size, liquidity, concentration).
7. **Suggested next step** — a process step only (request items, pass for now, route to reviewer).

Use the [investment memo template](../../templates/investment-memo-template.md) as the output structure.

## Instructions

- Draw only from the source material. Do not add facts, figures, market data, or claims not present in the inputs.
- Present the thesis as *the opportunity's own case* ("as presented"), never as your recommendation.
- Separate **confirmed/stated information** from **assumptions**. Mark inferred items *(assumption)*.
- Be specific in risks and diligence questions; generic risk lists are not useful. Tie each to something in the material.
- In *Potential fit*, describe considerations neutrally; do not render a verdict on whether to invest.
- Keep *Suggested next step* procedural — never "invest" or "pass" as a judgment, only the next process action.
- Flag every material gap under *Missing information*.

## Quality control

- **Missing information:** Deal material is usually incomplete. Actively identify and list what a competent investor would need that was not provided (financials, cap table, terms, references, legal structure).
- **Hallucination risk:** Do not supply market sizes, comparables, growth rates, or financial figures that are not in the source. If a number is not provided, say it is missing rather than estimating.
- **Confidentiality:** Treat the material as confidential. Do not introduce outside information about the company, founders, or counterparties.
- **Uncertainty:** Where the material is vague, mark items *(assumption)* and convert the ambiguity into a diligence question.

## Do not

- Do not recommend investing, passing, or sizing a position.
- Do not provide investment, legal, tax, or valuation advice.
- Do not invent financials, market data, comparables, or claims.
- Do not present the promoter's thesis as verified fact.
- Do not commit the office to any action or next step beyond a process suggestion.
- Do not omit the *Missing information* section.

## Example request

> "Using the investment-memo-screener skill, produce a first-pass memo from this material: [paste deal summary / deck notes / founder email]. Screen it against a generic mandate of early-stage software, $250k–$1M checks."

---

*This skill supports human judgment and produces an unverified screening draft for review. It does not provide investment, legal, tax, accounting, or compliance advice, makes no recommendation to invest, pass, or size a position, and does not authorize any decision, transaction, or communication. A competent person must verify all output before it is used.*
