---
name: vendor-review
description: Use this skill to evaluate a vendor proposal, renewal notice, service issue, or performance summary into a structured review. Produces a review covering the vendor overview, current relationship, key terms, service issues, cost considerations, risks, questions for the vendor, and a recommended process next step.
---

# Vendor Review

## Purpose

This skill turns vendor material — a proposal, renewal notice, service-issue summary, or performance update — into a structured review that helps an operator decide how to handle the relationship. It organizes terms, surfaces risks and service issues, frames the cost considerations, and produces the questions to put to the vendor. The output supports a human decision to renew, renegotiate, escalate, or replace; it does not make that decision or commit the office.

## When to use this

- Reviewing a vendor or service-provider renewal before a decision.
- Evaluating a new vendor proposal against the current arrangement.
- Documenting and structuring a service issue or performance concern.
- Preparing for a vendor negotiation or relationship review meeting.

## Inputs

Provide whatever you have; the skill works with partial material and flags gaps.

- **Vendor material:** proposal, renewal notice, contract excerpt, invoice, or service summary.
- **Service category** (e.g., IT/AV, custody, insurance brokerage, accounting, household, technology).
- **Relationship context:** how long, what they provide, how service has been.
- **Any known issues** or concerns.
- **Cost detail** as available (current vs. proposed).

## Output

Produce a review with these sections, in this order:

1. **Vendor overview** — who they are and what they provide.
2. **Current relationship** — tenure, scope, and how it has gone.
3. **Key terms** — table of the material terms (scope, price, length, renewal, termination).
4. **Service issues** — table of issues and their impact.
5. **Cost considerations** — current vs. proposed and what is driving change.
6. **Risks** — table of risks (switching cost, dependency, lock-in, performance).
7. **Questions for vendor** — specific questions to resolve before a decision.
8. **Recommended next step** — a process step only (renew, renegotiate, request info, benchmark, escalate, evaluate alternatives).

## Instructions

- Use only the information provided. Do not invent terms, prices, or service history.
- Frame cost considerations factually; do not assert that a price is "good" or "bad" without the basis. Note when benchmarking is needed.
- Separate **confirmed terms** from **assumptions.** Mark inferred items *(assumption)*.
- Keep *Recommended next step* procedural — a recommended *action in the process*, not an approval to sign or terminate.
- Make *Questions for vendor* specific to this vendor and material.
- Flag missing terms (auto-renewal, termination, SLAs) under *Questions for vendor* or as a noted gap.

## Quality control

- **Missing information:** Vendor material often omits the terms that matter most (termination, auto-renewal, SLAs, total cost). Identify and flag these gaps.
- **Hallucination risk:** Do not supply market pricing, comparables, or terms not in the source. If a term is absent, mark it *(missing)*.
- **Confidentiality:** Treat the material as confidential; introduce no outside information about the vendor.
- **Uncertainty:** Where pricing or value can't be assessed without a benchmark, say so rather than implying a judgment.

## Do not

- Do not approve, sign, renew, or terminate anything.
- Do not assert a price is fair or unfair without a stated basis.
- Do not invent terms, pricing, comparables, or service history.
- Do not provide legal advice on the contract; route contractual questions to counsel.
- Do not commit the office to any action beyond a process suggestion.

## Example request

> "Using the vendor-review skill, review this renewal notice and prepare questions for the vendor: [paste vendor material and relationship context]."

---

*This skill supports human judgment and produces an unverified review draft. It does not provide legal, tax, accounting, procurement, or compliance advice, does not assess whether pricing is fair, and does not approve, sign, renew, or terminate anything. Route contractual questions to counsel. A competent person must verify all terms before acting.*
