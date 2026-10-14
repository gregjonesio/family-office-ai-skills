# Contract Renewal Check

A skill that reads a service agreement that renews itself, with every amendment, against the provider's renewal letter and recent invoices, before anyone decides whether to renew: when the term really ends, the last day to give notice and how notice must be given, whether the letter states the terms the agreement actually contains, and whether the current charges match the fee schedule. It decides nothing and sends nothing, and it does not provide legal advice.

## What it does

Produces a check: the deadline at the top with the days remaining, the documents read in the order they take effect, each renewal, notice and price term as it reads after every amendment, quoted, the dates with every count shown, each statement in the renewal letter against the agreement, each invoice line against the fee schedule, what the documents cannot show, questions for the provider and for counsel, and action items for the office.

## Who uses it

Operators, chiefs of staff, office managers, and controllers who manage the office's service providers (IT support, security, records storage, property and household services) and keep its contract calendar.

## How to use it

1. Gather the agreement with its schedules, every amendment or change order, the provider's renewal letter or price notice, and one or two recent invoices. Provide only sanitized material, and use an approved environment for real contracts.
2. Invoke the skill and tell it today's date (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check every date count, figure and quoted clause against the documents, and read the amendments yourself for anything it missed.
4. Record the deadline the same day, labeled provisional, and have counsel confirm the deadline, the notice method and the address before treating them as settled. Plan to the earliest date the check supports. A reply to the provider's email is not necessarily notice under the agreement.
5. Drop any question the documents already answer, then put the rest to the provider or counsel.

## Try it on the test kit first

The [test kit](test-kit/) is a fictional managed IT services agreement with a known answer: an amendment titled as adding a location that changed the renewal terms in a section headed as administrative, a renewal letter that states them differently, and an invoice with charges the fee schedule does not contain. Run it in your own AI tool, score the result against the [answer key](test-kit/answer-key.md), and see [what happened when we ran it](test-kit/README.md#results-so-far).

## What its instructions tell the AI not to do

These are instructions to the AI, not guarantees; the recorded runs show it does not always follow them perfectly. Check every output.

- Provide legal, tax, accounting, or procurement advice.
- Recommend renewing, not renewing, renegotiating, or terminating.
- Draft, send, or confirm a notice or a reply, or treat a reply to the provider's letter as notice.
- Say whether the office is bound by a term or whether a charge is owed.
- Supply an index value, a market rate, or any figure the documents do not contain, or a reason for a change the documents do not explain.
- Contact the provider or counsel.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional agreement, amendment, renewal letter, and invoice.
- [examples/sample-output.md](examples/sample-output.md): the check produced from them.
- [test-kit/](test-kit/): the same documents with an answer key, for testing.

*Output is a draft for human review. Not legal, tax, accounting, or procurement advice. The office decides whether to renew; counsel confirms deadlines, notice methods, and the meaning of the agreement.*
