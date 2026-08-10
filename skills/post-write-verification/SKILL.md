---
name: post-write-verification
description: Use this skill after a person has approved and recorded a change in a system of record, to test independently whether the change actually landed and landed correctly. Compares the intended change against evidence read back through a different path and classifies the result as verified, absent, altered, duplicated, or indeterminate. It records nothing and posts nothing; it only tests what is already there.
---

# Post-Write Verification

## Purpose

A system reporting that a change succeeded is not evidence that the change exists. An interface can return success, return an identifier, and show a status of recorded, while nothing reached the underlying record. Everything downstream then treats the work as complete, and the discrepancy surfaces weeks later as an unexplained balance.

This skill closes that gap. After a person has approved and recorded a change, it compares what was intended against evidence read back through a **different path** than the one that wrote it, and reports a classified result rather than a pass or fail.

The single rule it exists to enforce: **an unverified change is a failed change, not a neutral one.**

## When to use this

- After any approved change is recorded in a ledger, register, or system of record.
- After a batch of changes, where one silent failure inside the batch is easy to miss.
- When a prior period's figures do not behave as expected and you need to establish what is actually recorded.
- Before relying on a change downstream: in a reconciliation, a report, or a close.

## Inputs

- **The intended change:** what was supposed to be recorded, field by field, as approved.
- **The approval record:** who approved it, when, and which specific object they approved.
- **Read-back evidence:** a report, export, or query result obtained **after** the change, ideally through a different interface than the one used to record it.
- **How the evidence was obtained:** which path, which interface, and its as-of time.
- **Any reported result** from the recording step, such as a returned identifier or status.

## Output

Produce a report with these sections, in this order:

1. **Verification summary** table: counts by outcome.
2. **Field-by-field comparison** for each change: intended value, observed value, and match or mismatch.
3. **Outcome classification** for each change, with the evidence supporting it.
4. **Independence assessment:** whether the read-back path was genuinely independent of the write path, and what that limits.
5. **Items requiring action**, with what to do and in what order.
6. **Gaps and assumptions.**

Use exactly these outcomes:

| Outcome | Meaning |
|---|---|
| Verified | Present in the read-back evidence and matching the intended change field for field |
| Absent | Reported as recorded, but not present in the evidence |
| Altered | Present, but one or more fields differ from what was approved |
| Duplicated | Present more than once from a single approval |
| Indeterminate | The evidence cannot establish presence or absence |

## Instructions

- Compare against the **approved** version of the change, not against a later description of it. If the approval record and the intended change disagree, report that as a finding in its own right.
- Compare every field that was approved, including date, amount, direction, account, entity, description, and period. A matching amount is not a match.
- State plainly how the read-back evidence was obtained. If it came through the same interface that recorded the change, say so and treat the result as weaker.
- **Treat indeterminate as a failure**, not as a neutral or passing result. Say what specific evidence would resolve it.
- Report absent and duplicated outcomes first. They are the ones that corrupt downstream work silently.
- Do not accept a returned identifier, a status field, or the absence of an error as evidence of presence. Note them as reported results, and evaluate them against the read-back evidence.
- Where a batch was recorded from one approval, verify each item, not the batch total. A correct total can contain offsetting errors.

## Quality control

- **Independence is the whole point.** An interface that recorded a change incorrectly will describe it incorrectly when asked about its own work. If independence cannot be established, the verification is weak and must say so.
- **Staleness:** if the evidence's as-of time precedes the recording, it cannot verify anything. Check this before comparing.
- **Scope errors look like passes.** Evidence drawn from the wrong account, entity, or period will show nothing and read as a clean absence. Confirm the evidence covers the right scope, and report the scope you checked.
- **A count of zero is a finding, not a result.** If the evidence returns nothing at all, distinguish "the change is absent" from "the query did not look where the change would be."
- **Partial batches:** verify item level, never batch total alone.
- **Hallucination risk:** do not infer that a change is present because it would be reasonable for it to be present.

## Do not

- Do not record, post, correct, reverse, or retry anything.
- Do not approve a change or re-approve one that failed.
- Do not report an outcome of verified on the basis of a success response, a returned identifier, or a status field.
- Do not treat indeterminate as acceptable.
- Do not fill in an unobserved field with what it should have been.
- Do not provide accounting, tax, or audit advice.

## Example request

> "Using the post-write-verification skill, check whether these approved entries actually landed. Here is what was approved, what the system reported, and a report export pulled afterward: [paste intended changes, approval record, reported results, and read-back evidence with its source and as-of time]."

---

*This skill supports human judgment and produces an unverified draft for review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It records nothing, corrects nothing, and reverses nothing. A verification result is itself a draft finding that a competent person must confirm before acting on it.*
