---
name: reconciliation-evidence-pack
description: Use this skill to assemble the evidence a person needs to reconcile an account. Tests two separate assertions, completeness and validity, using independently obtained source evidence rather than the ledger's own account of itself. Produces an aged reconciling-item schedule that separates timing differences from unexplained ones. It does not reconcile the account, does not sign off, and never reports that a balance ties.
---

# Reconciliation Evidence Pack

## Purpose

A reconciliation that reports a zero difference has not necessarily proved anything. Two errors in opposite directions net to zero, and that is a normal way for a reconciliation to pass while being wrong. So is a reconciliation that tests only one direction.

This skill assembles the evidence for a person to reconcile, structured around **two separate assertions** rather than a single difference figure, and using **independently obtained source evidence** rather than the ledger's own account of itself.

The person reconciles, concludes, and signs. This skill prepares what they need in order to do that honestly.

## The two assertions

They are not the same test, and passing one says nothing about the other.

| Assertion | Question | Failure looks like |
|---|---|---|
| **Completeness** | Is every source item represented in the ledger? | Activity occurred and was never recorded |
| **Validity** | Is every ledger item supported by a source item? | The ledger contains something the source does not support |

> **On independence.** Rolling a ledger balance forward using ledger activity is **not** an independent test of the ledger. It reuses the same population and will agree with itself. Independent evidence comes from outside the ledger: an institution's statement, a custodian report, a counterparty confirmation, or an export consumed by a separate system. Where only ledger-derived evidence is available, this skill still runs and reports that the test is weak.

## When to use this

- Before a person signs off on an account reconciliation.
- At period end, on any account that feeds reporting.
- When a balance has moved in a way nobody can explain.
- After entries have been recorded and verified, to test whether the resulting balance holds.

## Inputs

- **Ledger balance and activity** for the account and period.
- **Independent source evidence:** statement, custodian report, or confirmation, with its origin and as-of date.
- **Prior period's reconciling items**, if available.
- **Known outstanding items:** deposits in transit, unpresented payments, accruals.
- **The office's aging thresholds** for reconciling items, if set.

## Output

Produce a pack with these sections, in this order:

1. **Evidence inventory:** what was provided, where each piece came from, its as-of date, and whether it is independent of the ledger.
2. **Completeness test:** source items not represented in the ledger.
3. **Validity test:** ledger items not supported by source.
4. **Reconciling-item schedule:** every item, aged, and classified as a timing difference or unexplained.
5. **Gross movement summary:** the total of items in each direction, stated before any netting.
6. **What a person must still resolve** before concluding.
7. **Gaps, assumptions, and limits of this pack.**

## Instructions

- Run and report the two assertions **separately.** Never merge them into one difference figure.
- State the **gross** total of reconciling items in each direction before stating any net. A net figure appears only alongside its gross components.
- Classify every reconciling item as a **timing difference** (expected to clear, with the expected clearing basis stated) or **unexplained** (no known basis). Do not classify an item as timing because it is small.
- **Age every reconciling item** from the date it arose, not from the period end. Carry prior-period items forward and show how long they have been outstanding.
- Assess independence explicitly. Name the source of each piece of evidence and say whether it originated outside the ledger.
- If the evidence's as-of date does not align with the period end, say so and state what that leaves untested.
- Present findings as evidence for a person's conclusion. **Do not state a conclusion.**

## Quality control

- **A zero net difference is not a result.** Report it alongside the gross movements that produced it. If offsetting items exist, say so prominently.
- **One-directional testing is incomplete.** If only one assertion could be tested, the pack must say which one and what remains unknown.
- **Aging reveals what netting hides.** An item that has been outstanding across several periods is a finding regardless of size.
- **Scope errors read as clean.** Evidence covering the wrong account, entity, or date range will show few differences and look like a good result. Confirm and report the scope actually covered.
- **Stale evidence:** an as-of date earlier than the period end cannot support a period-end conclusion.
- **Hallucination risk:** do not supply an explanation for a difference that the material does not support. "Unexplained" is a valid and useful classification.

## Do not

- Do not reconcile the account, conclude that it is reconciled, or state that a balance ties.
- Do not sign off, or produce anything presented as a sign-off.
- Do not book, post, adjust, or propose a plug.
- Do not net differences without showing the gross components.
- Do not classify an item as a timing difference without stating the basis on which it is expected to clear.
- Do not treat the ledger's own roll-forward as independent evidence.
- Do not provide accounting, tax, or audit advice.

## Example request

> "Using the reconciliation-evidence-pack skill, assemble what I need to reconcile this account: [paste ledger balance and activity, the independent statement with its as-of date, prior reconciling items, and known outstanding items]."

---

*This skill supports human judgment and produces an unverified draft for review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It does not reconcile an account, does not conclude that a balance ties, and does not sign off. The reconciliation, the conclusion, and the sign-off are the responsibility of a competent person.*
