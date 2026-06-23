# Investment Memo Screener

A skill that converts raw opportunity material — a deal summary, pitch deck notes, a CIM excerpt, or a founder email — into a consistent first-pass investment memo. It standardizes the front of the deal-flow funnel and surfaces the right diligence questions. It is a screen, not a recommendation.

## What it does

Produces a structured memo: opportunity overview, the thesis as presented, key risks, diligence questions, missing information, potential fit against a generic mandate, and a suggested process next step.

## Who uses it

Investment analysts, deal-flow managers, chiefs of staff, and operators triaging inbound opportunities.

## How to use it

1. Gather the source material and any generic mandate context (see [SKILL.md](SKILL.md) → *Inputs*). Provide only sanitized material.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Treat the output as a **screen, not advice.** Verify every figure and claim against source; the memo presents the promoter's case, not a verified one.
4. Address the *Diligence questions* and *Missing information* before the opportunity advances.

## What it will not do

- It will not tell you to invest, pass, or size a position.
- It will not invent financials, market data, or comparables.
- It will not provide investment, legal, tax, or valuation advice.

## Files

- [SKILL.md](SKILL.md) — the workflow contract.
- [examples/sample-input.md](examples/sample-input.md) — a fictional founder email.
- [examples/sample-output.md](examples/sample-output.md) — the screening memo produced from it.

*Output is a draft screen for human review. Not investment, legal, or tax advice. No recommendation to invest is made or implied.*
