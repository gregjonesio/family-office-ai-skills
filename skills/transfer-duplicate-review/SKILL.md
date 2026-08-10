---
name: transfer-duplicate-review
description: Use this skill when source activity spans several accounts, to identify where one economic event has been represented more than once. Groups related source rows across accounts, classifies each group as an internal transfer, an inter-entity transfer, a transfer with a separate fee, a genuine external flow, a pending-and-settled pair, or unmatched, and reports which representations are duplicates. It suppresses nothing on its own and books nothing.
---

# Transfer and Duplicate Review

## Purpose

Money moving between accounts the office controls is **one economic event that arrives as several source rows**. Treated naively, each row looks like independent activity, and the same movement gets recorded twice or booked as income or expense.

The same problem appears within a single account when an institution publishes a charge twice, once on authorization and again on settlement, often with a different description and sometimes a different amount.

This skill groups related rows, names the single economic event behind each group, and identifies which rows are duplicate **representations** of that event rather than separate events.

> **An important distinction.** What may be suppressed is a duplicate *source representation*, never an accounting leg. An internal transfer is one event that still requires both a debit and a credit. This skill reduces double counting of source rows; it does not remove one side of a double entry, and it does not decide the accounting treatment of the event it identifies.

## When to use this

- Before preparing entries when source activity spans more than one account.
- When an account shows movements that appear to have no external counterparty.
- When an institution's feed publishes both pending and settled versions of the same charge.
- After a feed re-pull or re-import, when the same activity may have arrived twice.

## Inputs

- **Source rows** from every account that might be related, not just the account being worked.
- **Account and entity map:** which accounts belong to which legal entity.
- **Settlement window:** how many days a movement may take to appear on the other side, if known.
- **Tolerances** for amount variance, if the office has set them.
- **Fee conventions**, if the office has documented them.

## Output

Produce a report with these sections, in this order:

1. **Group summary** table: counts and totals by classification.
2. **Group detail:** for each group, the rows it contains, the single economic event proposed, and the evidence for grouping them.
3. **Duplicate representations:** the specific rows that restate an event already represented elsewhere.
4. **Requires a person:** every cross-entity group, every partial match, and anything unmatched.
5. **Unmatched rows** that appeared to be one side of a movement but have no counterpart.
6. **Gaps and assumptions.**

Use exactly these classifications:

| Classification | Meaning |
|---|---|
| Internal transfer | Between two accounts of the same legal entity |
| Inter-entity transfer | Between accounts of different legal entities |
| Transfer plus fee | A movement where an intermediary deducted a separate amount |
| Pending and settled pair | The same charge published twice by one institution |
| Genuine external flow | A real movement to or from an outside party |
| Unmatched | Appears to be one side of a movement, with no counterpart found |

## Instructions

- Search **across all provided accounts**, not only the account being worked. A movement whose counterpart sits in an account you were not given cannot be detected, and the report must say so.
- Group on opposite-signed amounts within the settlement window, then corroborate with description, reference, and counterparty before proposing a group.
- For each group, name the **one economic event** and identify which row is the primary representation and which are restatements.
- Treat **cross-entity groups differently.** A movement between two legal entities is not merely a deduplication question; it raises an intercompany or equity question that a person must answer. Never resolve it in this report.
- For pending and settled pairs, retain the link between the rows. Identify which representation survives, and preserve the reference to the one that does not.
- Where a fee was deducted in transit, report the gross movement and the fee separately rather than netting them.
- Report every suppression candidate with the criteria that produced it, so a person can disagree with a specific test rather than the conclusion.

## Quality control

- **Similar amount and timing is evidence, not proof.** Two unrelated movements of the same size within a few days are common. Say what corroborates each group beyond amount and date.
- **Suppression is destructive if wrong.** A row wrongly identified as a duplicate disappears from the work and is never missed. Prefer routing to a person over asserting a match.
- **Retain lineage.** Every identified duplicate must remain traceable to the event it restates.
- **Amounts may legitimately differ** between a pending and a settled version, for tips, foreign exchange, or final settlement. A difference does not disprove a pair, and a match does not prove one.
- **Do not net a fee** into the movement. Netting hides the fee permanently.
- **Partial coverage:** if accounts were not provided for every entity in the map, say which counterparts could not have been found.
- **Hallucination risk:** do not invent a counterpart row to complete a group.

## Do not

- Do not book, post, exclude, or delete anything.
- Do not decide the accounting treatment of a transfer, including whether an inter-entity movement is a payable, a loan, a contribution, or a distribution. That follows the office's agreements and policy, and a person applies it.
- Do not remove one side of a double entry. Duplicate representations are source rows, not accounting legs.
- Do not treat a cross-entity match as a simple duplicate.
- Do not net fees, or restate gross amounts as net.
- Do not provide accounting, tax, or audit advice.

## Example request

> "Using the transfer-duplicate-review skill, group these rows across our accounts and tell me where one movement is represented more than once: [paste source rows from all related accounts, the account and entity map, and the settlement window]."

---

*This skill supports human judgment and produces an unverified draft for review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It books nothing, excludes nothing, and determines no intercompany treatment. A competent person must verify every proposed grouping against source records before any row is treated as a duplicate.*
