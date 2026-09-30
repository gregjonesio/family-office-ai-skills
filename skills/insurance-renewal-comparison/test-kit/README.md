# Test kit: Insurance Renewal Comparison

A fictional homeowners renewal with a known answer, for checking whether an AI following [the skill](../SKILL.md) finds what a careful reader should, before you rely on it with a real renewal.

The broker's cover letter mentions three changes. Nine more are on the declarations pages and not in the letter. The [answer key](answer-key.md) lists all twelve and was written before any AI saw the documents.

## What is in it

- [01-expiring-declarations.md](01-expiring-declarations.md): last year's declarations page.
- [02-renewal-declarations.md](02-renewal-declarations.md): this year's renewal declarations page.
- [03-broker-cover-letter.md](03-broker-cover-letter.md): the letter that came with the renewal.
- [answer-key.md](answer-key.md): the changes, and the scoring rule.

Every figure and form number is invented. Names are placeholders.

## How to run it

1. Start a fresh session with your AI tool, with no other context loaded.
2. Give it [SKILL.md](../SKILL.md) as its instructions and documents 1 to 3. Do not give it the answer key, and do not tell it how many changes to look for or that any were planted.
3. Ask for the renewal comparison the skill describes.
4. Score the output against the [answer key](answer-key.md) using its scoring rule, and check every figure against the documents yourself.

Run it more than once if you can. One run shows what happened once, not how often it happens.

## Results so far

| Date | Instructions used | Found | Errors | Notes |
|---|---|---|---|---|
| 2026-09-30 | [Document Digest](../../document-digest/SKILL.md) (this skill did not exist yet) | 9 of 9 | None found | One loose summary of the letter; one broker question asked something the pages already answer (whether the storm deductible covers only named storms). Both flaws shaped this skill's instructions. |
| 2026-09-30 | This skill | 9 of 9 | None found | Every derived figure matched its arithmetic. No broker question asked what the pages already answer. Output: [examples/sample-output.md](../examples/sample-output.md). |

Both runs used a general-purpose AI model in a fresh session, one run each, on the documents in this folder. The first run used a version of the documents with invented names in place of the placeholders; the figures and layout were identical. A 9 of 9 on a short, clean test says nothing about how an AI will do on a real renewal, which is longer and includes policy forms whose wording can change without anything on the declarations page moving.

*Fictional test material for checking an AI workflow. Not insurance, legal, or tax advice, and not evidence that any output is reliable. A competent person must verify any comparison against the documents.*
