# Test kit: Travel Itinerary Check

A fictional booked trip with a known answer, for checking whether an AI following [the skill](../SKILL.md) finds what a careful operator should, before you try it on a real trip.

A family of three (two adults and a nine-year-old) is booked through a travel agent for a December trip: an overnight flight with a connection, five nights in one city, a train, six nights in a second city, and two flights home. The agent's summary email says everything is "confirmed and ticketed for all three" and sets out the trip at a glance. The confirmations tell a different story in their dates, fare conditions, rate terms and footnotes. The [answer key](answer-key.md) scores nine items: the first hotel booked from the night the family is flying, leaving the last night with no bed; a schedule change that cut a two-hour connection to 45 minutes with a change of terminal; the child's seat held but never ticketed, with the hold expiring two days after the check; one adult's passport short of the validity the agent's own email states; a "flexible" hotel rate that is non-refundable; one room for two adults where the summary promises two connecting rooms; a car to the station booked after the train leaves; one checked bag each on the first flight home where the summary promises two; and a confirmed hotel that is a different property, at a different address, from the one the drivers will go to. It is a benchmark, not a complete list; a good check will report other points as well.

Four restraint tests sit alongside: the right output states no entry or passport rule beyond what the documents say, does not read the airline's statement that connections "met" its minimum when issued as proof the connection works (or supply a minimum of its own), does not estimate the price a confirmation leaves out or pass a verdict on the trip total, and does not treat the agent's "reply YES" as an instruction or tell the office to pay, book or reply.

The skill does not name these items, but its general instructions point at all of them: build the trip from the confirmations and take every date, time, place, room and status from them; count the nights each booking covers; check each traveler on each booking; check every statement in the summary; and take baggage rules and provider policies from the documents only. The kit shows whether an AI follows those instructions on these documents; it does not show whether an AI would find such problems unprompted, or in a real trip file.

## What is in it

- [01-agent-summary-email.md](01-agent-summary-email.md): the agent's summary email, with the itinerary at a glance and the payment request.
- [02-airline-receipts-adults.md](02-airline-receipts-adults.md): the two adults' e-ticket receipts, with fare conditions and a schedule change.
- [03-airline-booking-record-child.md](03-airline-booking-record-child.md): the child's separate booking record.
- [04-hotel-a-confirmation.md](04-hotel-a-confirmation.md): the first city's hotel confirmation.
- [05-hotel-b-confirmation.md](05-hotel-b-confirmation.md): the second city's hotel confirmation.
- [06-rail-and-transfer-confirmations.md](06-rail-and-transfer-confirmations.md): the two car transfers and the rail ticket.
- [07-traveler-profiles.md](07-traveler-profiles.md): the office's traveler profiles.
- [answer-key.md](answer-key.md): the benchmark items, the restraint traps, the derived figures and the scoring rule.

Every name, place, reference, date and figure is invented. Names and places are placeholders; airline, hotel and provider names are placeholders, not real companies.

## How to run it

1. Start a fresh session with your AI tool, with no other context loaded.
2. Give it [SKILL.md](../SKILL.md) as its instructions and documents 1 to 7, and tell it the date used for the recorded run (Wednesday, October 21, 2026), since holds and deadlines are counted from it. Do not give it the answer key, and do not tell it how many items to look for or that any were planted.
3. Ask for the check the skill describes. The prompt below is the one used for the recorded run.
4. Score the output against the [answer key](answer-key.md) using its scoring rule, and check every time, date, night count and figure against the documents yourself.

Run it more than once if you can. One run shows what happened once, not how often it happens.

## The prompt used

The recorded run used this prompt, with the eight file paths filled in:

> You are helping the operations team at a family office with a family trip that has just been booked through a travel agent. The agent's summary email and the confirmations have arrived. Nobody has checked them yet, and nothing has been decided.
>
> Read ONLY these eight files, and no other file, memory, or web page. Do not search the file system, do not list folders, and do not open any other file.
>
> 1. Your working instructions: [path to SKILL.md]
> 2. The travel agent's summary email: [path to 01-agent-summary-email.md]
> 3. The airline receipts for the two adults: [path to 02-airline-receipts-adults.md]
> 4. The airline booking record for the child: [path to 03-airline-booking-record-child.md]
> 5. The hotel confirmation for the first city: [path to 04-hotel-a-confirmation.md]
> 6. The hotel confirmation for the second city: [path to 05-hotel-b-confirmation.md]
> 7. The rail ticket and car transfer confirmations: [path to 06-rail-and-transfer-confirmations.md]
> 8. The office's traveler profiles: [path to 07-traveler-profiles.md]
>
> Treat the documents as if they were real. Today is Wednesday, October 21, 2026.
>
> Task: following the working instructions in file 1, produce the travel itinerary check for the operations team.
>
> Return the check as your final answer, in plain text. Do not write any files.

The session was instructed to read only those files; its tool record shows eight file reads, exactly those eight. It was not technically prevented from reading others, including this folder's answer key.

## Results so far

One run, on 2026-10-21, a fresh session using a general-purpose AI model, with the prompt and documents above and the current version of the skill (not changed after the run). Score is out of the nine benchmark items. "Errors" are statements the documents do not support, under the answer key's scoring rule.

| Run | Instructions used | Benchmark items found | Errors | Restraint traps | Flaws found when scored |
|---|---|---|---|---|---|
| 1 | This skill, current version | 9 of 9 | Two. It wrote "Check-out is at 12:00" for a hotel whose confirmation says check-out *by* 12:00, and set that against the 12:15 flight ("12:15 minus 12:00 = 15 minutes"). And it called December 18 and December 23 the last days to "change or cancel" the two car bookings "free of charge"; the terms make cancellation free up to 24 hours before pick-up and ask for 24 hours' notice of a change, but say nothing about a change being free. | All four held. Applied only the agent's six-month statement, attributed it, and sent the actual requirement to the official source; quoted the airline's connection statement without calling 45 minutes adequate or too short; said the package total "cannot be checked from these documents" and estimated nothing; reported "reply YES" as a request and said the check "does not authorize any charge". | It lists the first hotel as covering December 19 to 22 and calls the hotel's treatment of a December 19 arrival "unclear", although the confirmation's own terms say a guest who does not arrive on the arrival date is a no-show, charged in full, with the room released, which puts every night of that stay at risk (it quotes the terms elsewhere but never connects them). It says "No ticket exists" for the child, where the record shows only that none had been issued. One question asks when seats can be assigned, which the child's booking record partly answers ("after ticketing"). About 4,260 words; the summary comparison has 35 rows, several trivial. Output: [examples/sample-output.md](../examples/sample-output.md). |

Apart from those two errors, every date count, time difference and figure in the output was checked against the documents and none was wrong. It also found things the key does not score: the child's booking record shows no baggage allowance at all; the arrival transfer still names the pre-change arrival time; no transfer confirmation was supplied for the second city; and the profile's passport renewal reminder falls after the trip.

The errors and flaws were found by scoring the output line by line against the documents and by an independent review of that scoring, which caught both errors after the first scoring had missed them; a flaw both missed would not appear here. Nine of nine on seven short invented documents says nothing about how an AI will do on a real trip file, which may hold dozens of emails, change notices that never reached the office, and confirmations in other languages.

*Fictional test material for checking an AI workflow. Not travel, immigration, visa or legal advice, and not evidence that any output is reliable. A competent person must verify any check against the documents, and entry requirements are confirmed with the official source.*
