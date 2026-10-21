# Entity Compliance Calendar

A skill that builds a twelve-month compliance calendar for one entity from the entity's own documents: the formation certificate, the governing agreement, state notices, registered agent letters, the accountant's emails and the office's register entry. Every date in the calendar is traced to the clause that sets it, with the count shown, so a person can check it and enter it in the office's own calendar. It files nothing, and it is not legal, tax or compliance advice.

## What it does

Produces a calendar: anything already passed or due within 30 days first, the documents read, a dated table of every filing, report, meeting and renewal in the period with its source quoted and its arithmetic shown, the recurring rules behind the dates, obligations that depend on a date not yet set, places where two documents disagree, what the documents do not cover, questions for counsel, the accountant or the provider, and action items for the office.

## Who uses it

Operators, chiefs of staff, controllers and office managers who keep an office's entity register and compliance calendar, and anyone taking over an entity's administration.

## How to use it

1. Gather the entity's formation documents, its governing agreement and every amendment, each state's notices, the registered agents' letters, the accountant's and counsel's emails that set dates, and the office's register entry. Provide only sanitized material, and use an approved environment for real entity documents.
2. Invoke the skill with today's date and the period to cover (see the *Example request* in [SKILL.md](SKILL.md)).
3. Check every date, count and day of the week against the documents yourself, and read the governing agreement's definitions for anything it missed.
4. Have counsel and the accountant confirm the obligations, the rules and anything the calendar flags as passed or in conflict, then enter the dates in the office's own calendar.
5. Drop any question the documents already answer, then put the rest to the right person.

## Try it on the test kit first

The [test kit](test-kit/) is a fictional holding LLC with seven documents and a known answer: dates counted from four different starting points (a filing date, a fiscal year ending June 30, a calendar taxable year and a formation month), a weekend rule that covers some dates and not others, and a meeting deadline and a manager's term that have already passed. Run it in your own AI tool, score the result against the [answer key](test-kit/answer-key.md), and see [what happened when we ran it](test-kit/README.md#results-so-far).

## What its instructions tell the AI not to do

These are instructions to the AI, not guarantees; check every output.

- Provide legal, tax, accounting or compliance advice.
- Add an obligation, a deadline, a rule or an amount from outside the documents.
- Say whether the entity is in good standing, or what follows if a date is missed.
- Decide which of two disagreeing documents governs, or what an ambiguous clause means.
- Make or submit a filing, report, payment or reply, or share a password, PIN or login.
- Contact a state, an agency, a provider, counsel or the accountant.

## Files

- [SKILL.md](SKILL.md): the workflow contract.
- [examples/sample-input.md](examples/sample-input.md): the fictional entity's documents.
- [examples/sample-output.md](examples/sample-output.md): the calendar built from them.
- [test-kit/](test-kit/): the same documents with an answer key, for testing.

*Output is a draft for human review. Not legal, tax, accounting or compliance advice. Counsel and the accountant confirm the obligations and the dates.*
