# Capital Call Notice Check

A skill that checks a capital call notice against the fund's previous notice and the office's record of the fund's terms before anyone acts on it: does the arithmetic hold, does the due date give the notice period the agreement requires, is each term the notice relies on the one in the record, and what changed since the last notice that the cover note does not say. It verifies nothing and pays nothing, and it does not provide legal, tax, or investment advice.

## What it does

Produces a check: the documents compared and what is missing, the notice as printed, each arithmetic and date check with the working shown, each term checked against the record, every field that changed since the previous notice and whether the cover note mentions it, the payment instructions field by field against the previous notice and the record on file, what the documents cannot show, questions for the fund or administrator, and action items for the office.

## Who uses it

Operators, chiefs of staff, controllers, and executive assistants who receive capital call notices and route them for approval.

## How to use it

1. Gather the new notice, the previous notice from the same fund, the office's record of the fund's terms (commitment, fee basis, notice period, default interest, payment instructions on file, verified contacts, and the office's wire verification procedure), and the cover email. Provide only sanitized material, and use an approved environment for real notices.
2. Invoke the skill (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check every figure and every change it reports against the documents, and read both notices yourself for anything it missed.
4. If any payment instruction field differs from the previous notice or the record, a person verifies the instructions by calling a contact already on file at a number already on file. Nothing in this output, and nothing printed in the notice or the email, substitutes for that call.
5. Drop any question the documents already answer, then put the rest to the fund or administrator through a verified channel.

## Check it before you rely on it

The [test kit](test-kit/) is a fictional capital call with a known answer: the cover email mentions three things and the notice carries eight more that do not check or changed without a word. Run it in your own AI tool, score the result against the [answer key](test-kit/answer-key.md), and see [what happened when we ran it](test-kit/README.md#results-so-far).

## What it will not do

These are instructions to the AI, not guarantees. Check every output.

- It will not provide legal, tax, investment, or accounting advice.
- It will not approve, pay, stage, or release a wire, or say whether the call should be paid.
- It will not verify payment instructions, or treat a number printed in a notice or email as a way to verify them.
- It will not conclude that a notice is genuine or fraudulent.
- It will not compute a figure from a basis the documents do not state, supply a reason for a change the documents do not explain, or name a company the documents do not name.
- It will not contact the fund, the administrator, or a bank, or send anything.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional terms record, two notices, and a cover email.
- [examples/sample-output.md](examples/sample-output.md): the check produced from them.
- [test-kit/](test-kit/): the same documents with an answer key, for testing.

*Output is a draft for human review. Not legal, tax, investment, or accounting advice. A person verifies payment instructions through a contact and number already on file before any wire; counsel or the administrator settles questions of interpretation.*
