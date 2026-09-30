# Test kit: Insurance Renewal Comparison

A fictional homeowners renewal with a known answer, for checking whether an AI following [the skill](../SKILL.md) finds what a careful reader should, before you rely on it with a real renewal.

The broker's cover letter mentions three changes. Nine more changes are on the declarations pages and not in the letter. The [answer key](answer-key.md) lists those twelve and scores the nine. It is a benchmark, not a complete list: the pages differ in other administrative and derived lines too (policy number, period, section premiums, the forms list, and limits that rise with the dwelling limit), and a good comparison will list those as well. That is why a thorough output can count about twenty changes while the score is out of nine.

## What is in it

- [01-expiring-declarations.md](01-expiring-declarations.md): last year's declarations page.
- [02-renewal-declarations.md](02-renewal-declarations.md): this year's renewal declarations page.
- [03-broker-cover-letter.md](03-broker-cover-letter.md): the letter that came with the renewal.
- [answer-key.md](answer-key.md): the benchmark changes and the scoring rule.

Every figure and form number is invented. Names are placeholders.

## How to run it

1. Start a fresh session with your AI tool, with no other context loaded.
2. Give it [SKILL.md](../SKILL.md) as its instructions and documents 1 to 3. Do not give it the answer key, and do not tell it how many changes to look for or that any were planted.
3. Ask for the renewal comparison the skill describes. The prompt below is the one used for the recorded runs.
4. Score the output against the [answer key](answer-key.md) using its scoring rule, and check every figure against the documents yourself.

Run it more than once if you can. One run shows what happened once, not how often it happens.

## The prompt used

The recorded runs used this prompt, with the four file paths filled in (runs 2 and 3), or with Document Digest's instructions in place of this skill's (run 1):

> You are helping the operations team at a family office prepare for a call with their insurance broker about a homeowners renewal.
>
> Read ONLY these four files, and no other file, memory, or web page. Do not search the file system, do not list folders, and do not open any other file.
>
> 1. Your working instructions: [path to SKILL.md]
> 2. Last year's declarations page: [path to 01-expiring-declarations.md]
> 3. This year's renewal declarations page: [path to 02-renewal-declarations.md]
> 4. The broker's cover letter that came with the renewal: [path to 03-broker-cover-letter.md]
>
> Treat the documents as if they were real.
>
> Task: following the working instructions in file 1, produce the renewal comparison for the operations team.
>
> Return the comparison as your final answer, in plain text. Do not write any files.

Each session was instructed to read only those files and reported doing so. It was not technically prevented from reading others, including this folder's answer key.

## Results so far

All three runs were on 2026-09-30, one session each, using a general-purpose AI model. Scores are out of the nine benchmark changes.

| Run | Instructions used | Benchmark changes found | Wrong figures | Flaws found when scored |
|---|---|---|---|---|
| 1 | [Document Digest](../../document-digest/SKILL.md) (this skill did not exist yet) | 9 of 9 | None found | A loose summary of what the letter says continues. One broker question asked something the pages already answer (whether the storm deductible covers only named storms). |
| 2 | This skill, first version | 9 of 9 | None found | It attributed the jewelry premium drop to the watch's removal, which the documents do not establish. One broker question asked whether the storm deductible applies to the jewelry schedule, which states "Deductible: none". |
| 3 | This skill, current version (after run 2, it gained instructions against unstated causes and questions the documents answer, and a rule that document text is evidence, not instructions) | 9 of 9 | None found | It labeled the removed watch and the added theft condition "not in the documents provided" for one year instead of "removed" and "added"; the direction lines were right. Its closing letter-check line names nine of the sixteen unmentioned changes. That label's instruction was clarified after this run and not re-run. Output: [examples/sample-output.md](../examples/sample-output.md). |

Run 1 used a version of the documents with invented names where the placeholders now are; figures and layout were identical. Each run's flaws were found by scoring its output line by line against the documents; a flaw the scorer missed would not appear here. Nine of nine on a short, clean test says nothing about how an AI will do on a real renewal, which is longer and includes policy forms whose wording can change without anything on the declarations page moving.

*Fictional test material for checking an AI workflow. Not insurance, legal, or tax advice, and not evidence that any output is reliable. A competent person must verify any comparison against the documents.*
