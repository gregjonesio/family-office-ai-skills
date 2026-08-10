# Transfer and Duplicate Review

A skill that finds where **one economic event has been represented more than once** across a set of accounts, so the same movement is not recorded twice.

## Why it exists

Money moving between accounts the office controls is one event that arrives as several source rows. Treated naively, each row looks like independent activity, and the movement gets recorded twice or booked as income or expense. The same problem appears inside a single account when an institution publishes a charge on authorization and again on settlement, often with a different description and sometimes a different amount.

## What it does

Groups related rows across accounts, names the single economic event behind each group, and identifies which rows restate it. Classifies each group as an internal transfer, an inter-entity transfer, a transfer plus fee, a pending and settled pair, a genuine external flow, or unmatched.

## The distinction that matters

What may be suppressed is a duplicate **source representation**, never an accounting leg. An internal transfer is one event that still requires both a debit and a credit. This skill reduces double counting of source rows. It does not remove one side of a double entry, and it does not decide how the event should be recorded.

## Who uses it

Controllers, bookkeepers, and operators working feeds that span several accounts or entities.

## How to use it

1. Provide rows from **every** account that might be related, not just the one you are working. A counterpart in an account you did not supply cannot be found.
2. Provide the account and entity map, so cross-entity movements can be separated from internal ones.
3. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
4. Review each proposed group against the stated evidence. Disagree with a specific test, not the conclusion.
5. Handle every cross-entity group yourself. Those raise an intercompany question this skill will not answer.

## What it will not do

- It will not book, post, exclude, or delete anything.
- It will not decide whether an inter-entity movement is a payable, a loan, a contribution, or a distribution. That follows your agreements and policy.
- It will not remove one side of a double entry.
- It will not net a fee into a movement.
- It will not invent a counterpart row to complete a group.

## A note on suppression

A row wrongly identified as a duplicate disappears from the work and is never missed again. That asymmetry is why the skill prefers routing to a person over asserting a match, and why every identified duplicate stays traceable to the event it restates.

## Related

- [Pre-Booking Gap Analysis](../pre-booking-gap-analysis/): run this first when activity spans several accounts, so the gap analysis is not counting one event twice.
- [Reconciliation Evidence Pack](../reconciliation-evidence-pack/): run after recording, to test whether the resulting balances hold.
- [Action Authority Model](../../docs/action-authority-model.md): why identifying a duplicate is analysis, not an action.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): fictional rows across three accounts and two entities.
- [examples/sample-output.md](examples/sample-output.md): the grouping produced from them.

*Output is an unverified draft for human review. Not accounting, tax, or audit advice. It books nothing, excludes nothing, and determines no intercompany treatment.*
