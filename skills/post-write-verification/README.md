# Post-Write Verification

A skill that tests whether an approved change **actually landed** in a system of record, using evidence read back through a different path than the one that wrote it.

## Why it exists

A system reporting success is not evidence that anything happened. An interface can return success, hand back an identifier, and display a status of recorded, while nothing reached the underlying record. Everything downstream then treats the work as complete, and the discrepancy surfaces much later as a balance nobody can explain.

The rule this skill enforces: **an unverified change is a failed change, not a neutral one.**

## What it does

Compares each approved change against read-back evidence and classifies the result as verified, absent, altered, duplicated, withdrawn, or indeterminate. It also assesses whether the evidence was genuinely independent of the write path, because a system that recorded something incorrectly will describe it incorrectly when asked about its own work.

## Two things it needs that are easy to skip

**The direction of intent for each item:** created, modified, or removed. An absent object is a failure under the first two and a success under the third, and nothing in the evidence tells you which. That is the difference between *absent* and *withdrawn*, and a verification that cannot separate them will report successful cleanups as failures.

**The target state, when you are verifying a remediation.** A fresh write asks *did this land*. A remediation asks *did this land and did the balance reach where it was supposed to go*. Every entry can verify while the account still misses its target.

## Who uses it

Controllers, bookkeepers, operators, and anyone who has recorded changes through an interface they did not build and cannot see inside.

## How to use it

1. Gather the approved change, the approval record, whatever the system reported, and read-back evidence obtained **after** the change (see [SKILL.md](SKILL.md) → *Inputs*).
2. Obtain that evidence through a different interface where you can: a report, an export, a separate query. Note which path you used and its as-of time.
3. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
4. Work the absent and duplicated items first. Those are the ones corrupting downstream work right now.
5. Treat any indeterminate result as failed, and go get the evidence that would resolve it.

## What it will not do

- It will not record, post, correct, reverse, or retry anything.
- It will not report *verified* on the basis of a success response, a returned identifier, or a status field.
- It will not treat *indeterminate* as acceptable.
- It will not fill in an unobserved field with what it should have been.

## A note on scope

Before trusting any read-back, confirm what the query actually looked at rather than what you asked it to look at. Account searches by name or number can silently resolve to several accounts, and a truncated result can contain rows from none of the one you meant while looking completely plausible.

A large confident result set is more dangerous than an empty one. An empty result prompts you to check. A full one does not.

## A note on independence

If the only evidence available comes through the same interface that recorded the change, this skill still runs, but it will say the verification is weak. That is the honest result. A verification that inherits the write path's blind spot reproduces the blind spot.

## Related

- [Action Authority Model](../../docs/action-authority-model.md): this skill is state 5. Nothing is complete without it.
- [Pre-Booking Gap Analysis](../pre-booking-gap-analysis/): run before entries are prepared, to establish what is already recorded.
- [Reconciliation Evidence Pack](../reconciliation-evidence-pack/): run after, to test whether the resulting balance holds from both directions.

- [Standing Context](../../docs/standing-context.md): the conventions and structure this skill defers to. Where they are not written down, its output degrades to "ask a person" no matter how good the inputs are.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional batch of approved entries with read-back evidence.
- [examples/sample-output.md](examples/sample-output.md): the verification report produced from it.

*Output is an unverified draft finding for human review. Not accounting, tax, or audit advice. It records nothing and corrects nothing.*
