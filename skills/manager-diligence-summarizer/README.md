# Manager Diligence Summarizer

A skill that distills investment manager and fund materials — pitch books, DDQs, factsheets, call notes — into a consistent, diligence-ready summary an allocator can review and compare. It is a diligence summary, not a recommendation.

## What it does

Produces a structured summary: strategy overview, team, track record (with caveats), fees and liquidity, portfolio construction, risk factors, key questions, and follow-up diligence items.

## Who uses it

Allocators, investment analysts, RIAs, and operators running a manager diligence pipeline.

## How to use it

1. Gather the manager materials and a strategy descriptor (see [SKILL.md](SKILL.md) → *Inputs*). Provide only sanitized material.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Treat the output as a **summary of unverified, promotional material.** Independently confirm all track record and fee figures.
4. Use the *Key questions* and *Follow-up diligence items* to drive the next diligence stage.

## What it will not do

- It will not recommend allocating to or avoiding the manager.
- It will not invent or estimate returns, AUM, or fees.
- It will not provide investment, legal, tax, or valuation advice.

## Files

- [SKILL.md](SKILL.md) — the workflow contract.
- [examples/sample-input.md](examples/sample-input.md) — fictional manager materials.
- [examples/sample-output.md](examples/sample-output.md) — the diligence summary produced from them.

*Output is a draft summary for human diligence. Not investment, legal, or tax advice. No recommendation to allocate is made or implied.*
