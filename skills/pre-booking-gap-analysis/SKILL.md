---
name: pre-booking-gap-analysis
description: Use this skill before preparing any accounting entries from source activity. Where the platform maintains its own review queue or unmatched flag, that flag is taken as a claim to be tested rather than an answer to be adopted. It compares a period's source items against what the ledger already contains and classifies every item as already booked, partially booked, covered by an aggregate entry, pending, a duplicate representation, genuinely missing, or ambiguous. Produces a coverage table and a draft entry packet covering only the genuinely missing items. It books nothing and reconciles nothing.
---

# Pre-Booking Gap Analysis

## Purpose

The most common failure when an AI assists with bookkeeping is additive: it prepares entries because source activity exists, without first establishing what the ledger already contains. The result is duplicate accounting that is expensive to find and worse to unwind.

This skill inverts the order. It reads what is already booked, diffs the source population against it, and proposes draft entries only for the genuinely missing remainder. Everything uncertain is routed to a person rather than resolved by inference.

## When to use this

- Before preparing entries from a bank, custodian, or subledger feed for any period.
- When picking up a period someone else started, or resuming work after a gap.
- When a feed has been re-pulled, re-imported, or re-dated and the coverage is unclear.
- Before a close, to establish what remains genuinely unbooked rather than what looks unbooked.

## Inputs

Provide whatever you have. The skill works with partial material and flags what is missing.

- **Source population:** the transactions, statement lines, or notices for a defined period.
- **Existing ledger activity** for the same accounts and period, including drafts and unposted items if available.
- **The platform's own claim about what is unrecorded**, where one exists: a review queue, an unmatched flag, a status field. Provide it as an input. **It is a claim to be tested, not an answer to be adopted.** A system that failed to record something may also have failed to flag it, and a system that flags an item as unrecorded may simply not recognize the entry that already covers it.
- **Period boundaries** and any hard date floor (for example, a conversion date before which nothing should be booked).
- **Matching tolerances:** acceptable variance in amount and date, if the office has set them.
- **Prior decisions:** items previously reviewed and deliberately excluded, if available.

## Output

Produce a report with these sections, in this order:

1. **Coverage summary** table: counts and totals by classification.
2. **Classification detail** table: one row per source item with date, amount, description, classification, and the evidence for that classification.
3. **Genuinely missing** items, the only population eligible for a draft entry.
4. **Requires a person** items: partial matches, aggregate-covered items, and anything ambiguous, each with the specific question to resolve.
5. **Draft entry packet** for the genuinely missing items only, presented for review.
6. **Gaps and assumptions:** what was not provided and what was inferred.

Use exactly these classifications:

| Classification | Meaning |
|---|---|
| Already booked | A ledger entry matches this item |
| Partially booked | Booked at a different amount, or split across entries that do not sum to it |
| Covered by aggregate | Included inside a summary or batch entry rather than individually |
| Pending | Present in the source but not yet final or settled |
| Duplicate representation | The same economic event as another source item |
| Genuinely missing | No ledger entry corresponds to it |
| Ambiguous | Cannot be classified from the material provided |

## Instructions

- Establish what is already booked **before** examining what could be booked. State the ledger population you compared against, including its date range and which accounts it covers.
- **Where the platform supplies its own unrecorded flag, reconcile your classification against it and report both.** Agreement is evidence. Disagreement is a finding in either direction: an item the platform calls unrecorded that you find already booked is a probable duplicate about to be created, and an item the platform considers handled that you find genuinely missing is the more dangerous case, because nothing will prompt anyone to look at it.
- Normalize dates, amounts, and references before matching, and say how you normalized them.
- Treat the absence of an exact description or date match as **insufficient** evidence that something is unbooked. An entry can be booked under a different memo, on a different date, or inside an aggregate.
- Classify every source item. An unclassified item is a defect in the output, not an acceptable omission.
- Draft entries only for the *genuinely missing* population. Partial, aggregate-covered, and ambiguous items go to a person with a specific question.
- Where a hard date floor applies, list items outside it separately and do not draft entries for them.
- Show your totals both ways: source total, booked total, and the difference the draft packet is meant to close.
- Mark every inferred item *(assumption)* and every absent item *(missing)*.

## Quality control

- **Completeness:** the classification counts must sum to the source population. If they do not, say so rather than presenting a partial view.
- **The arithmetic is not the answer.** A gap that nets to zero can still contain offsetting errors. Report the gross movements, not just the net.
- **Aggregate entries hide coverage.** Before classifying anything as missing, check whether a summary or batch entry already includes it.
- **Re-pulled feeds duplicate.** If the source population appears to overlap a prior import, flag it rather than classifying the overlap as missing.
- **Stale ledger views mislead.** If the ledger extract's as-of date is older than the source period, say that the comparison is incomplete.
- **Hallucination risk:** do not invent ledger entries, account codes, amounts, or a chart of accounts that was not provided.

## Do not

- Do not book, post, or apply anything.
- Do not reconcile an account or assert that a balance ties.
- Do not select an accounting treatment, an account code, or a policy the office has not provided.
- Do not classify an item as missing on the basis of a description or date mismatch alone.
- Do not resolve an ambiguous item by choosing the more likely reading.
- Do not provide accounting, tax, or audit advice.

## Example request

> "Using the pre-booking-gap-analysis skill, compare this period's source activity against the ledger activity below and tell me what is genuinely unbooked: [paste source population, ledger activity, period, and any tolerances]."

---

*This skill supports human judgment and produces an unverified draft for review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It books no entry, reconciles no account, and closes no period. A competent person must verify every classification and every draft entry against source records before anything is recorded.*
