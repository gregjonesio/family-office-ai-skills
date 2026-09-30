---
name: insurance-renewal-comparison
description: Use this skill to compare an insurance renewal against the expiring policy, line by line, and check the broker's cover letter against what actually changed. Produces a change table with last year's and this year's terms, whether the letter mentions each change, a check of the letter's own statements, derived figures with their arithmetic shown, what the documents cannot show, questions for the broker, and action items. It does not provide insurance, legal, or tax advice.
---

# Insurance Renewal Comparison

## Purpose

This skill compares a renewal (declarations pages, schedules, and any forms provided) against the expiring policy, item by item, and checks the broker's cover letter or renewal summary against what actually changed. A cover letter is a summary, and a summary is a choice about what to include: a letter can be accurate and still leave out a change that matters to the insured. The skill lists every change it can find in the documents, marks which ones the letter mentions, shows what the documents cannot tell you, and frames every coverage concern as a question for the broker. It makes the renewal legible before the renewal call. It is **not** insurance, legal, or tax advice, and it does not judge whether coverage is adequate.

## When to use this

- Preparing for a renewal call with a broker, before the renewal is accepted.
- Checking a broker's renewal summary against the declarations pages.
- Reviewing a renewal where the premium changed and the explanation covers only part of the picture.
- Building a record of what changed at each renewal for the policy file.

## Inputs

Provide whatever you have; the skill works with partial material and says what is missing.

- **Last year's declarations pages** (or the expiring binder), including any schedules.
- **This year's renewal declarations pages**, including any schedules.
- **The broker's cover letter** or renewal summary, if one came with the renewal.
- **Policy forms for both years**, if available. Without them, wording changes cannot be compared.
- **Known changes in circumstances** (a new property, a sold item, a renovation), if relevant.

## Output

Produce a comparison with these sections, in this order:

1. **Documents compared:** what was provided for each year, and what was not (for example, "policy forms not provided").
2. **Change table:** one row per change, with the item, last year's term, this year's term, the direction of the change in plain words, and whether the letter mentions it (*mentioned*, *not mentioned*, or *partly mentioned*). Quote both terms exactly as the documents state them.
3. **Letter check:** each statement in the letter checked against the pages: *matches*, *true but incomplete* (with what it leaves out), *does not match*, or *cannot be checked from these documents*.
4. **Derived figures:** any figure the documents imply but do not state (a percentage deductible in dollars, a limit that moves with an automatic adjustment), each labeled *(derived)* with its arithmetic shown.
5. **What the documents do not show:** wording, definitions, and terms the provided documents cannot answer (form wording when only form numbers or edition dates changed, undefined terms, whether a limit is per occurrence or aggregate).
6. **Questions for the broker:** grouped by topic, each tied to a row in the change table or an item in section 5.
7. **Action items for the office:** concrete next steps a person takes (confirm with whoever manages the property, request the forms, verify this comparison against the documents).

## Instructions

- **Compare every line of both years**, not only the sections the letter discusses: coverages, limits, percentages, deductibles, endorsements, conditions, schedules, named insureds, premises details, form numbers and edition dates, and premium by section.
- **Check schedules item by item.** Count the items in each year's schedule and match them one to one. A removed, added, or revalued item is a change even when the schedule total is described as continuing.
- **Treat a changed form edition date as a change.** Say that the wording may have changed and that the declarations cannot show how.
- **Quote both terms exactly.** Do not paraphrase a limit, a deductible, or a condition in the change table.
- **Do not rely on the letter.** Use it only for the *mentioned* column and the letter check. A change counts whether or not the letter mentions it.
- **Label derived figures** *(derived)* and show the calculation from the stated terms. If a figure depends on an assumption (for example, that terms stay the same next year), state the assumption.
- **Describe direction, not merit.** Say that a limit fell from 100% to 25%, not that coverage got worse. Whether a change is acceptable is a question for the insured and the broker.
- **Before writing a question, check whether the documents already answer it.** If they do, state the answer from the documents in the change table and do not ask it.
- **Route interpretation to the broker.** What a term means under the policy, how a claim would be settled, and why a change was made are questions, not findings.
- Preserve confidentiality; policy documents carry personal, property, and asset details.

## Quality control

- **Completeness:** After drafting, walk both years' documents from top to bottom once more and confirm every difference appears in the change table. Recount each schedule.
- **Missing information:** If a year's documents are partial, or forms are not provided, say so in section 1 and section 5 rather than assuming standard terms.
- **Hallucination risk:** Do not invent limits, deductibles, endorsements, conditions, or explanations for a change. Re-read and remove anything not supported by the documents.
- **Arithmetic:** Recheck every derived figure and every percentage change against the stated terms.
- **Uncertainty:** When a term is ambiguous or undefined in the documents provided, flag it in section 5 and ask; do not resolve it.

## Do not

- Do not provide insurance, legal, or tax advice.
- Do not state whether coverage is adequate, whether a change is acceptable, or whether a limit is too high or too low.
- Do not recommend accepting, declining, or changing the renewal, or moving to another carrier.
- Do not interpret what a term means under the policy when the form wording is not provided.
- Do not invent limits, deductibles, conditions, schedule items, or reasons for a change.
- Do not treat the cover letter as a complete list of changes.
- Do not contact the broker or carrier, and do not send the questions. A person does that.

## Example request

> "Using the insurance-renewal-comparison skill, compare this renewal with last year's policy and check the broker's cover letter against it: [paste last year's declarations pages], [paste this year's renewal declarations pages], [paste the cover letter]."

---

*This skill produces a line-by-line comparison to make an insurance renewal legible before it is discussed with a broker. It is not insurance, legal, or tax advice, does not judge whether coverage is adequate, and does not recommend accepting, declining, or changing a renewal. Have the broker and, where needed, counsel review coverage questions before acting. A competent person must verify the comparison against the documents. Use creates no professional or fiduciary relationship.*
