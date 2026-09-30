# Insurance Renewal Comparison

A skill that compares an insurance renewal against the expiring policy, line by line, and checks the broker's cover letter against what actually changed. A cover letter is a summary; it can be accurate and still leave out a change that matters. It does not provide insurance, legal, or tax advice.

## What it does

Produces a comparison: the documents compared and what is missing, a change table with last year's and this year's terms and whether the letter mentions each change, a check of the letter's own statements, derived figures with their arithmetic shown, what the documents cannot show, questions for the broker, and action items.

## Who uses it

Operators, chiefs of staff, and executive assistants preparing for a renewal call, before the renewal is accepted.

## How to use it

1. Gather last year's declarations pages, this year's, and the broker's cover letter. Add both years' policy forms if you have them; without them, wording changes cannot be compared. Provide only sanitized material, and use an approved environment for real policy documents.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check every change it reports against the documents, and look over the pages yourself for anything it missed.
4. Drop any question the documents already answer, then send the rest to the broker before the call and ask for written answers.

## Check it before you rely on it

The [test kit](test-kit/) is a fictional renewal with a known answer: the broker's letter mentions three changes and the pages hold nine more. Run it in your own AI tool, score the result against the [answer key](test-kit/answer-key.md), and see [what happened when we ran it](test-kit/README.md#results-so-far).

## What it will not do

These are instructions to the AI, not guarantees. Check every output.

- It will not provide insurance, legal, or tax advice, or judge whether coverage is adequate.
- It will not recommend accepting, declining, or changing a renewal, or moving to another carrier.
- It will not interpret policy wording it was not given, or invent limits, conditions, or reasons for a change.
- It will not contact the broker or send anything.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional renewal, last year's page, and the cover letter.
- [examples/sample-output.md](examples/sample-output.md): the comparison produced from it.
- [test-kit/](test-kit/): the same documents with an answer key, for testing.

*Output is a draft for human review. Not insurance, legal, or tax advice. Have the broker and, where needed, counsel review coverage questions before acting.*
