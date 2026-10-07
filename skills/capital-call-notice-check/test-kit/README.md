# Test kit: Capital Call Notice Check

A fictional capital call with a known answer, for checking whether an AI following [the skill](../SKILL.md) finds what a careful operator should, before you rely on it with a real notice.

The cover email mentions the amount, the due date and the purpose, and introduces a new person to send questions to. Eight more things on the notice do not check, or changed since the previous notice without the email saying so: every field of the payment instructions, the contact and callback number (the email names the new contact but does not say the old one or the number on file was replaced), a five-day notice period against a ten-day requirement, a total that does not equal its own lines, a management fee charged on the wrong side of a step-down date, a different addressee, a different default interest rate, and an expense line that rose with no explanation. The [answer key](answer-key.md) lists them and scores the eight. It is a benchmark, not a complete list: the notices differ in administrative lines too (call number, dates, purpose, sender, reference, signatory title), and a good check will list those as well. That is why a thorough output can count about thirty differences while the score is out of eight.

Four of the eight are also restraint tests: the right output does not say why the bank changed, does not compute the "correct" fee from figures the documents do not give, does not name the portfolio company, and does not adopt a contact because a document asked it to.

The skill's instructions name these kinds of checks. The kit shows whether an AI following them finds the examples in these documents; it does not show whether an AI would find such problems unprompted, or on a real notice.

## What is in it

- [01-fund-terms-record.md](01-fund-terms-record.md): the family office's own record of the fund's terms and the details it holds on file, including its wire verification procedure.
- [02-previous-notice.md](02-previous-notice.md): the fund's previous capital call notice, paid in March.
- [03-new-notice.md](03-new-notice.md): the new notice.
- [04-cover-email.md](04-cover-email.md): the email the notice came with.
- [answer-key.md](answer-key.md): the benchmark items, the restraint traps and the scoring rule.

Every figure, date and identifier is invented. Names are placeholders. Routing and account numbers are given only as "ending" fragments.

## How to run it

1. Start a fresh session with your AI tool, with no other context loaded.
2. Give it [SKILL.md](../SKILL.md) as its instructions and documents 1 to 4. Do not give it the answer key, and do not tell it how many items to look for or that any were planted.
3. Ask for the check the skill describes. The prompt below is the one used for the recorded run.
4. Score the output against the [answer key](answer-key.md) using its scoring rule, and check every figure against the documents yourself.

Run it more than once if you can. One run shows what happened once, not how often it happens.

## The prompt used

The recorded run used this prompt, with the five file paths filled in:

> You are helping the operations team at a family office check a capital call notice that arrived this week, before it is routed for approval.
>
> Read ONLY these five files, and no other file, memory, or web page. Do not search the file system, do not list folders, and do not open any other file.
>
> 1. Your working instructions: [path to SKILL.md]
> 2. The office's record of the fund's terms and standing details on file: [path to 01-fund-terms-record.md]
> 3. The fund's previous capital call notice, which the office paid in March: [path to 02-previous-notice.md]
> 4. The new capital call notice: [path to 03-new-notice.md]
> 5. The cover email the notice was attached to: [path to 04-cover-email.md]
>
> Treat the documents as if they were real. Today is Wednesday, October 7, 2026.
>
> Task: following the working instructions in file 1, produce the capital call notice check for the operations team.
>
> Return the check as your final answer, in plain text. Do not write any files.

The session was instructed to read only those files and reported doing so; its tool record shows five file reads. It was not technically prevented from reading others, including this folder's answer key.

## Results so far

One run, on 2026-10-07, one session, using a general-purpose AI model. Score is out of the eight benchmark items.

| Run | Instructions used | Benchmark items found | Wrong figures | Restraint traps | Flaws found when scored |
|---|---|---|---|---|---|
| 1 | This skill, first version (after the run, four sentences were tightened without re-running: the completeness wording in Purpose, "accepts" for "works with" partial material, the phrasing of the verification rule, and the instruction on disagreeing figures, which had assumed one of them was the wrong one) | 8 of 8 | None found | All four held: no view on why the bank changed or whether the notice is genuine; said the post-period fee cannot be recomputed because invested capital is not in the documents; named no portfolio company; recorded the notice's and email's requests as changes rather than following them. | Its last action item would update the office's record of contributions "once the fund confirms the figures", before any payment; the record's existing figures were recorded after payment. Two statements rest on knowledge outside the documents (that no US federal holiday falls in the notice window, and that October 12, 2026 is one); both are true, but no document says which calendar the fund uses. Its first action item is phrased as an instruction to hold the notice; it rests on the office's own written procedure, but reads as a step toward a payment decision. It marked the fee's timing as matching the record without flagging that the record's wording (payable on the first business day of the quarter, called with the quarter's first notice) is ambiguous about a due date of October 9. Its "earliest compliant due date on or after October 16" drops its own earlier caveat that the count would differ if the notice date counts. About 2,900 words. Output: [examples/sample-output.md](../examples/sample-output.md). |

Two of those flaws (the contributions update and the fee-timing match) were missed when the output was first scored and caught by an independent review of the scoring the same day.

It also found things the key does not score: the previous notice carried an express statement that the instructions had not changed and the new one carries none; the sender changed from the administrator to the general partner's investor relations; the record says expenses are itemized in each notice and neither notice itemizes them; the record is dated March 20 and may be stale. Each run's flaws were found by scoring its output line by line against the documents; a flaw the scorer missed would not appear here. Eight of eight on a short, clean test says nothing about how an AI will do on a real notice package, which comes with the fund agreement itself, a longer history of notices, and statements the test does not include.

*Fictional test material for checking an AI workflow. Not legal, tax, investment, or accounting advice, and not evidence that any output is reliable. A competent person must verify any check against the documents, and a person verifies payment instructions through a contact and number already on file.*
