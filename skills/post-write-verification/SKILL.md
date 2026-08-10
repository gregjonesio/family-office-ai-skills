---
name: post-write-verification
description: Use this skill after a person has approved and recorded a change in a system of record, to test independently whether the change actually landed and landed correctly. Compares the intended change against evidence read back through a different path and classifies each result as verified, absent, altered, duplicated, withdrawn, or indeterminate. Handles remediations, where the question is not only whether entries landed but whether the balance reached its target. It records nothing and posts nothing; it only tests what is already there.
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

- **The intended change**, and **its direction**: whether each item was meant to be *created*, *modified*, or *removed*. Absence means opposite things depending on the answer, so this is not optional.
- **The form the intent exists in.** A structured payload, a prepared entry packet, or a written description are all workable. Say which you have. A written description is weaker evidence than a payload, because it cannot be compared field by field, and the report must say so rather than implying a precision it does not have.
- **The approval record:** who approved it, when, and which specific object they approved. Where the approval identifies a category rather than an object, say so.
- **Read-back evidence:** a report, export, or query result obtained **after** the change, ideally through a different interface than the one used to record it.
- **How the evidence was obtained:** which path, which interface, its as-of time, and **the scope it actually covered**, not the scope you asked for.
- **Any reported result** from the recording step, such as a returned identifier or status.

**For a remediation**, add:

- **The prior known-bad state:** what the account or record read before the change, and why that was wrong.
- **The expected corrected state:** what it should read afterward, and the arithmetic connecting the two.

Verifying a remediation is a different question from verifying a fresh write. A fresh write asks *did this land*. A remediation asks *did this land and did it move the balance to where it was supposed to go*. An entry can land perfectly and still leave the account wrong.

## Output

Produce a report with these sections, in this order:

1. **Scope confirmation:** the identifiers the evidence query actually resolved to, and confirmation that the returned population belongs to the intended scope.
2. **Verification summary** table: counts by outcome.
3. **Field-by-field comparison** for each change: intended value, observed value, and match or mismatch. Where intent exists only as a written description, compare what it specifies and say what could not be compared.
4. **Outcome classification** for each change, with its direction of intent and the evidence supporting it.
5. **Target state**, where a remediation was verified: prior, expected, observed, and whether the target was achieved.
6. **Independence assessment:** whether the read-back path was genuinely independent of the write path, and what that limits.
7. **Items requiring action**, with what to do and in what order.
8. **Gaps and assumptions.**

Use exactly these outcomes:

| Outcome | Meaning |
|---|---|
| Verified | The intended state was achieved: present and matching where creation was intended, absent where removal was intended |
| Absent | Creation or modification was intended and reported as recorded, but the object is not present in the evidence |
| Altered | Present, but one or more fields differ from what was approved |
| Duplicated | Present more than once from a single approval |
| Withdrawn | Absent, and absence *was* the intent: an archive, reversal, or supersession. Where a replacement was intended, that replacement is verified separately |
| Indeterminate | The evidence cannot establish presence or absence |

**Absent and Withdrawn are the same observation with opposite meanings.** The object is not there in both cases. One is a failure and one is a success, and only the stated direction of intent distinguishes them. A verification that cannot tell them apart will report successful remediations as failures and mask genuine losses as intentional.

Where a **remediation** was verified, also report:

| | |
|---|---|
| Prior state | What it read before |
| Expected state | What it should read after |
| Observed state | What it reads now |
| Target achieved | Yes or no, independent of whether the individual entries verified |

## Instructions

- Compare against the **approved** version of the change, not against a later description of it. If the approval record and the intended change disagree, report that as a finding in its own right.
- **State the direction of intent for every item before classifying it.** Creation, modification, or removal. An absent object is a failure under the first two and a success under the third.
- Where the intent exists only as a written description rather than a structured payload, say so plainly and limit the comparison to the fields the description actually specifies. Do not present a narrative match as a field-by-field one.
- **Where a target state was specified, test it separately from the individual items.** Every entry can verify while the balance still misses its target, and every entry can be individually unremarkable while the target is met by accident.
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
- **A keyword or fuzzy account search will silently widen.** Asking for one account by name or number can resolve to many, and a truncated result set may contain rows from none of the account you asked about while looking entirely plausible. Read back the identifiers the query actually resolved to and confirm each returned row belongs to the intended scope. A large, confident result set is not evidence that the query was correctly aimed, and it is more dangerous than an empty one because nothing prompts you to check.
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
