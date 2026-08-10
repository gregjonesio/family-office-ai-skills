# Reconciliation Evidence Pack

A skill that assembles the evidence a person needs to reconcile an account, structured so that a passing result actually means something.

## Why it exists

A reconciliation reporting a zero difference has not necessarily proved anything. Two errors in opposite directions net to zero, and that is a normal way for a reconciliation to pass while being wrong. So is a reconciliation that only tests one direction.

## What it does

Tests **two separate assertions** rather than producing a single difference figure:

| Assertion | Question | Failure looks like |
|---|---|---|
| **Completeness** | Is every source item represented in the ledger? | Activity occurred and was never recorded |
| **Validity** | Is every ledger item supported by a source item? | The ledger contains something the source does not support |

Then produces an aged reconciling-item schedule that separates timing differences from unexplained ones, and states gross movements before any net.

## On independence

Rolling a ledger balance forward using ledger activity is **not** an independent test of the ledger. It reuses the same population and will agree with itself. Independent evidence comes from outside the ledger: an institution's statement, a custodian report, a counterparty confirmation. Where only ledger-derived evidence is available, the skill still runs and reports that the test is weak.

## Who uses it

Controllers, bookkeepers, and reviewers preparing to sign off on an account.

## How to use it

1. Gather the ledger balance and activity **and** independent source evidence, noting where each came from and its as-of date.
2. Include prior-period reconciling items so aging carries forward.
3. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
4. Read the two assertions separately. Passing one says nothing about the other.
5. Look at the aging before the net. An item outstanding across several periods is a finding regardless of size.
6. Reach the conclusion yourself. This pack does not contain one.

## What it will not do

- It will not reconcile the account, conclude that it is reconciled, or state that a balance ties.
- It will not sign off.
- It will not book, adjust, or propose a plug.
- It will not net differences without showing the gross components.
- It will not call something a timing difference without stating why it should clear.
- It will not invent an explanation. *Unexplained* is a valid and useful classification.

## Related

- [Post-Write Verification](../post-write-verification/): run before this, to confirm the entries you think are recorded actually are.
- [Pre-Booking Gap Analysis](../pre-booking-gap-analysis/): run before entries are prepared, to establish what is already recorded.
- [Quarter-End Close](../../playbooks/quarter-end-close.md): where this sits in a period close, and why the reconciliation and sign-off stay human.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional ledger and statement with reconciling items.
- [examples/sample-output.md](examples/sample-output.md): the evidence pack produced from them.

*Output is an unverified draft for human review. Not accounting, tax, or audit advice. It does not reconcile an account, conclude that a balance ties, or sign off.*
