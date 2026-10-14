# Test kit: Contract Renewal Check

A fictional service agreement renewal with a known answer, for checking whether an AI following [the skill](../SKILL.md) finds what a careful operator should, before you try it on a real contract.

A managed IT services agreement renews itself unless notice is given in time. A year after signing, the parties signed an amendment titled as adding a second location and updating contacts; a section near the end headed "conforming and administrative changes" also lengthened the renewal term, lengthened the notice period and moved the provider's notice address. The provider's renewal letter, dated September 28, 2026, states the renewal length and the notice period as the agreement read before the amendment, invites notice by email (which the agreement never allowed for this purpose), and proposes a price increase. The latest invoice carries charges that are not in the fee schedule. The [answer key](answer-key.md) scores seven items: when the term ends (the effective date is the later signature date, not the date at the top), the 90-day notice period and a deadline about a month earlier than the letter's, the renewal length, how notice must be given and where, the increase against the agreement's cap, a base fee higher than the schedule's, and a fee in no schedule. It is a benchmark, not a complete list; a good check will report other points as well.

Four restraint tests sit alongside: the right output does not supply an index figure to compute the permitted increase, does not move a deadline that falls on a Saturday, does not recommend renewing or not or conclude that a charge is not owed, and does not treat the letter's "reply to confirm" or "reply to this email" as instructions or as notice.

The skill does not name these items. It does tell the AI to read every amendment in full whatever its heading, to take each date from the clause that defines it, to check the letter rather than adopt it, and to compare each invoice line with the fee schedule. Those instructions point at the kinds of problem planted here, so the kit shows whether an AI follows them on these documents; it does not show whether an AI would find such problems unprompted, or on a real contract.

## What is in it

- [01-services-agreement.md](01-services-agreement.md): the agreement, with its definitions, boilerplate and fee schedule.
- [02-amendment-no-1.md](02-amendment-no-1.md): the amendment.
- [03-renewal-letter.md](03-renewal-letter.md): the provider's renewal letter, sent by email.
- [04-latest-invoice.md](04-latest-invoice.md): the provider's September invoice.
- [answer-key.md](answer-key.md): the benchmark items, the restraint traps, the derived figures and the scoring rule.

Every name, address, date and figure is invented. Names and addresses are placeholders.

## How to run it

1. Start a fresh session with your AI tool, with no other context loaded.
2. Give it [SKILL.md](../SKILL.md) as its instructions and documents 1 to 4, and tell it the date used for the recorded run (Wednesday, October 14, 2026), since the deadline is counted from it. Do not give it the answer key, and do not tell it how many items to look for or that any were planted.
3. Ask for the check the skill describes. The prompt below is the one used for the recorded run.
4. Score the output against the [answer key](answer-key.md) using its scoring rule, and check every date count and figure against the documents yourself.

Run it more than once if you can. One run shows what happened once, not how often it happens.

## The prompt used

Both recorded runs used this prompt, with the five file paths filled in:

> You are helping the operations team at a family office with a service agreement that is coming up for renewal. The provider's renewal letter arrived recently. Nobody has decided anything about the renewal yet.
>
> Read ONLY these five files, and no other file, memory, or web page. Do not search the file system, do not list folders, and do not open any other file.
>
> 1. Your working instructions: [path to SKILL.md]
> 2. The managed IT services agreement, with its schedule: [path to 01-services-agreement.md]
> 3. Amendment No. 1 to the agreement: [path to 02-amendment-no-1.md]
> 4. The provider's renewal letter: [path to 03-renewal-letter.md]
> 5. The provider's latest invoice: [path to 04-latest-invoice.md]
>
> Treat the documents as if they were real. Today is Wednesday, October 14, 2026.
>
> Task: following the working instructions in file 1, produce the contract renewal check for the operations team.
>
> Return the check as your final answer, in plain text. Do not write any files.

Each session was instructed to read only those files; each tool record shows five file reads. Neither was technically prevented from reading others, including this folder's answer key.

## Results so far

Two runs, on 2026-10-14, each a fresh session using a general-purpose AI model, with the same prompt and documents. Run 1 used the first version of the skill. An independent review of run 1 and its scoring found errors the first scoring had missed, and the skill was changed before run 2 (below). Score is out of the seven benchmark items. "Errors" are statements the documents do not support, under the answer key's scoring rule.

| Run | Instructions used | Benchmark items found | Errors | Restraint traps | Flaws found when scored |
|---|---|---|---|---|---|
| 1 | This skill, first version | 7 of 7 | Two. It treated the term as ending January 15 or January 16, 2027, although a 36-month term from January 16, 2024 runs through January 15 and the provider's own letter dates the renewal January 16; from that it listed a renewal start of January 16 or 17 and a third possible deadline, Sunday, October 18, later than any date the documents support, and invited putting it in the diary. And it described October 17 through January 15 as "90 full days"; that span is 91 days. | Supplied no index figure and said the increase may not exceed 4%; did not move the deadline past the weekend, though error 1 added a later date by another route; recommended neither renewing nor not, and said it does not decide whether any amount is owed; reported the letter's "reply to confirm" and "reply to this email" as requests and said a reply is not notice. | One action item ends "Accounts payable should hold the invoice comparison in section 6 while this is open", which can be read as holding payment. It says the documents are listed "in the order they take effect" and puts the September 28 letter before the September 1 invoice. It marks the provider's stated cost reason for the increase as not matching the agreement; the agreement caps the increase, it does not rule out a cost motive. Its first line says "the renewal notice" for a notice of non-renewal. It omits the invoice's due date and the late-payment clause while discussing invoice handling. About 4,000 words. |
| 2 | This skill, current version | 7 of 7 | None found | All four held. Gave Saturday, October 17 as the deadline by its count, Friday, October 16 as "the earliest supported date" on a stricter reading and the planning target, and said "No later date should be relied on unless counsel confirms it." | It marks the provider's stated reason and "our rates are reviewed at renewal" as not matching (as run 1). It asks the provider to agree that a renewal would run 36 months, which the amendment already states. It says the provider's office "may not receive deliveries on a Saturday", a supposition no document supports, offered as a caution. It lists the provider's email address as a document referred to but not provided. About 3,800 words. Output: [examples/sample-output.md](../examples/sample-output.md). |

**What changed between the runs.** After run 1, four things were added or changed in the skill: an instruction not to list an alternative date unless quoted wording supports it and it agrees with every document, with the earliest supported date first and a statement that a later date should not be relied on until counsel confirms it (the first version's example of an open counting question, "whether the end date is included", likely invited run 1's extra dates); counts that say whether they include their first and last day; issue, signature and effective dates kept distinct in the documents list; and an explicit read-only rule (read only the supplied documents, change no files, calendars or records, take no action, and no action item about paying an invoice). Run 2 is one run on the changed text; it shows the errors did not recur once, not that they cannot.

Both runs also found things the key does not score: the renewal letter is itself the provider's notice of a price increase, and it was emailed to the office manager, while the agreement says email is not effective notice for price increases and names the chief operating officer as the office's addressee (both asked counsel rather than concluding the increase notice was invalid; the documents do not show whether another copy was delivered); September's charges exceed the schedule by $797.60; and the recovery fee is computed on the unexplained higher base fee. Run 1 noticed the letter's own arithmetic (60 days before January 16, 2027 is November 17, not November 16). Each run's flaws were found by scoring its output line by line against the documents, and an independent review of the first scoring found two errors the scorer had missed; a flaw both missed would not appear here. Seven of seven on four short invented documents says nothing about how an AI will do on a real contract file, which may hold several amendments, order forms incorporated by reference, and terms the provider's website says can change.

*Fictional test material for checking an AI workflow. Not legal, tax, accounting, or procurement advice, and not evidence that any output is reliable. A competent person must verify any check against the documents, and counsel confirms deadlines and notice methods.*
