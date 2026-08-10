# Pre-Booking Gap Analysis

A skill that establishes what a ledger already contains **before** anyone prepares entries from source activity, so the work covers only the genuine gap.

## Why it exists

The default failure mode when AI assists with bookkeeping is additive. Source activity exists, so entries get prepared, without first checking what is already recorded. The result is duplicate accounting, which is expensive to find and worse to unwind. This skill inverts the order: read the ledger first, diff against it, and draft only the remainder.

## What it does

Classifies every source item as already booked, partially booked, covered by an aggregate entry, pending, a duplicate representation, genuinely missing, or ambiguous. Produces a coverage table, a list of items needing a person's decision, and a draft entry packet limited to the genuinely missing population.

## Who uses it

Controllers, bookkeepers, family office operators, and anyone picking up a period that someone else started.

## How to use it

1. Gather the source population **and** the existing ledger activity for the same accounts and period (see [SKILL.md](SKILL.md) → *Inputs*). Provide only sanitized material.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check the coverage counts sum to your source population. If they do not, the analysis is incomplete.
4. Work the *Requires a person* list yourself. Those items are routed there because inference is not safe, not because the analysis ran out of room.
5. Verify every draft entry against source records before recording anything.

## What it will not do

- It will not book, post, or apply anything.
- It will not reconcile an account or assert that a balance ties.
- It will not choose an account code or accounting treatment your office has not provided.
- It will not classify something as missing just because the description or date does not match.
- It will not resolve an ambiguous item by picking the more likely reading.

## Related

- [Reconciliation Evidence Pack](../reconciliation-evidence-pack/): run after entries are recorded, to test whether the balance actually holds.
- [Transfer and Duplicate Review](../transfer-duplicate-review/): use first when the source population spans several accounts, so one economic event is not counted twice.
- [Action Authority Model](../../docs/action-authority-model.md): where this sits in the five states, and why a draft packet is not an action.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional source population and ledger extract.
- [examples/sample-output.md](examples/sample-output.md): the coverage analysis produced from it.

*Output is an unverified draft for human review. Not accounting, tax, or audit advice. It books no entry, reconciles no account, and closes no period.*
