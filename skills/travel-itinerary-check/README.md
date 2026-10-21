# Travel Itinerary Check

A skill that reads every confirmation for a booked trip (airline receipts and booking records, hotel confirmations, rail tickets, car transfers) against the travel agent's summary and the office's traveler profiles, before anyone relies on the trip: which nights each booking covers, the booked times of every connection and handoff, each traveler's ticket and booking status, and where the summary differs from the confirmations, for a person to check. It books, changes, cancels and pays for nothing, and it is not travel, immigration or legal advice.

## What it does

Produces a check: the time-sensitive items first (holds that expire, payment dates, cancellation deadlines) with the days remaining, the documents read, the trip day by day and night by night as the confirmations record it with every connection time and night count shown, each traveler's status on each booking, each statement in the agent's summary against the confirmations, what each confirmation says about price, payment and cancellation, what the documents cannot show, questions for the agent, and action items for the office.

## Who uses it

Executive assistants, chiefs of staff, office managers and operators who arrange or check principal and family travel and keep the trip sheet that travelers, drivers and hosts rely on.

## How to use it

1. Gather the agent's summary and every confirmation for every traveler, including any change notices, and the travelers' profiles. Provide only sanitized material, and use an approved environment for real travel documents; leave document numbers out unless the check needs them.
2. Invoke the skill and tell it today's date (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check every time, date, night count and status against the confirmations yourself, and read the fare and rate conditions for anything it missed.
4. Deal with the time-sensitive items the same day. Confirm passport, visa and entry requirements with the official source for each destination; the check reports only what the documents say.
5. Drop any question the documents already answer, then put the rest to the agent or the provider.

## Try it on the test kit first

The [test kit](test-kit/) is a fictional family trip with a known answer: an agent's summary that says everything is confirmed and ticketed, and seven documents that tell a different story in their dates, fare conditions, rate terms and footnotes. Run it in your own AI tool, score the result against the [answer key](test-kit/answer-key.md), and see [what happened when we ran it](test-kit/README.md#results-so-far).

## What its instructions tell the AI not to do

These are instructions to the AI, not guarantees; the recorded runs show what it did on one trip. Check every output.

- Provide travel, immigration, visa, legal, tax or insurance advice, or state entry requirements the documents do not state.
- Book, hold, ticket, change, cancel or pay for anything, or authorize a charge.
- Reply to or contact the agent or any provider.
- Recommend a booking, a provider, a route or a change of plans.
- Supply a price, a rule, a minimum connection time or any figure the documents do not contain.
- Treat the agent's summary as a complete or correct account of the bookings.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): a fictional agent's summary, confirmations and traveler profiles.
- [examples/sample-output.md](examples/sample-output.md): the check produced from them.
- [test-kit/](test-kit/): the same documents with an answer key, for testing.

*Output is a draft for human review. Not travel, immigration, visa, legal or insurance advice. The office decides what to do with the agent and the providers, and confirms entry requirements with the official source.*
