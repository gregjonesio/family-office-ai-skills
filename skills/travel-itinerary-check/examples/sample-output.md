# Sample output: Travel Itinerary Check

The output of a fresh AI session given the current [SKILL.md](../SKILL.md) and the seven fictional documents in [sample-input.md](sample-input.md) (the same documents as the [test kit](../test-kit/)), on 2026-10-21, reproduced verbatim. This is run 1 in the [test kit results](../test-kit/README.md#results-so-far). The exact prompt is in the [test kit README](../test-kit/README.md#the-prompt-used). The session was instructed to read only those eight files; it was not technically prevented from reading others.

**Known errors and flaws in this output**, found when it was scored against the [answer key](../test-kit/answer-key.md) and when that scoring was independently reviewed, and left in place rather than edited out:

- **Error.** Question 10 says "Check-out is at 12:00", and section 3 sets "12:15 minus 12:00 = 15 minutes". The second hotel's confirmation says check-out *by* 12:00, a latest time, not a fixed one.
- **Error.** Section 1 calls December 18 and December 23 the last days to "change or cancel" the two car bookings "free of charge". The provider's terms make cancellation free up to 24 hours before pick-up and ask for 24 hours' notice of a change; they say nothing about a change being free.
- Section 3 lists the first hotel as covering December 19 to 22, and section 7 calls the hotel's treatment of a December 19 arrival "unclear", although the confirmation's own terms (quoted in section 6) say a guest who does not arrive on the arrival date is treated as a no-show, charged the full stay, with the room released.
- Section 2 says "No ticket exists" for the child; the record shows only that no ticket had been issued.
- Question 11 asks when seats can be assigned; the child's booking record says seats can be assigned after ticketing.
- About 4,260 words; section 5 has 35 rows, several of them trivial.

It found all nine benchmark items, all four restraint traps held, and apart from the two errors above no date count, time difference or figure checked was wrong. It is an unverified draft for human review, not travel, immigration, visa or legal advice. Entry and passport requirements are confirmed with the official source before anyone relies on them.

```text
TRAVEL ITINERARY CHECK: [Family] December 2026 trip (Agency ref TA-26-4471)
Prepared Wednesday, October 21, 2026. This is a draft for a person to check against the documents. It is not travel, immigration or legal advice. I have not booked, changed, cancelled, paid for or replied to anything.

======================================================================
1. TIME-SENSITIVE ITEMS
======================================================================

- Fri Oct 23, 2026, 23:59 [Home City] time (2 days): Traveler C's flights are held but not ticketed, and the hold has a time limit. The booking record says: "Ticket: NOT ISSUED" and "Unticketed bookings are cancelled automatically after the time limit. Space and fare are not guaranteed after cancellation." The quoted fare of USD 6,870.00 is guaranteed only if the ticket is issued by that time. Source: Doc 3, QX9R4L.
- Mon Nov 2, 2026 (12 days): the agent says a balance of $31,420.00 is due. The email asks the office to reply "YES" so the agent charges the card on file. That is a request recorded in the email; nothing has been done about it. Source: Doc 1.
- Fri Dec 18, 2026 (58 days): this is the first travel day. Traveler B's passport expires March 2, 2027, which is earlier than the six-month validity the agent's email states (arithmetic in section 4). Source: Doc 7 against Doc 1.
- Fri Dec 18, 2026 (58 days): Hotel A's confirmation gives an arrival date of 18 December. The rate cannot be cancelled, changed or refunded, and it carries a no-show clause tied to "the arrival date". The transport documents show the travelers reaching [City A] on 19 December. Source: Doc 4.
- Fri Dec 18, 2026 (58 days): the last day to change or cancel the arrival transfer GP-20931 free of charge. The provider requires 24 hours' notice before pick-up on 19 December. Source: Doc 6.
- Mon Dec 21, 2026, 18:00 [Hotel B] time (61 days): the end of free cancellation at Hotel B. After that, cancellations and no-shows are charged the first night. The booking currently covers one room for 2 adults (section 4). Source: Doc 5.
- Wed Dec 23, 2026 (63 days): no lodging is shown for the night of 23 December in [City A]. Source: Docs 4 and 6.
- Wed Dec 23, 2026, 08:30 (63 days): the last time to change or cancel the departure transfer GP-20932 free of charge. Its pick-up time of 08:30 on 24 December is 18 minutes after the train leaves (section 3). Source: Doc 6.
- No renewal date is set before the trip. Traveler B's profile says "Renewal reminder set for January 2027", which is after the trip. Source: Doc 7.

======================================================================
2. DOCUMENTS READ
======================================================================

- Doc 1: Agent's summary email, Fri Oct 9, 2026, 4:52 PM. Agency ref TA-26-4471. It covers all three travelers and records no change notice.
- Doc 2: [Airline A] e-ticket receipts, issued 06OCT26. Booking QX7T2M.
  - Traveler A: ticket 999 4417203361.
  - Traveler B: ticket 999 4417203362.
  - Records a schedule change processed 02OCT26 on [A] 2207.
- Doc 3: [Airline A] booking confirmation, booked 06OCT26. Booking QX9R4L for Traveler C (CHD), linked to QX7T2M. It records the same 02OCT26 schedule change. No ticket has been issued.
- Doc 4: [Hotel A] [City A] Airport confirmation 8830417. Guest: Traveler A, with 2 adults and 1 child. No document date is printed; it says the stay was charged on 06 October 2026.
- Doc 5: [Hotel B] confirmation HB-55102. Guest: Traveler A, occupancy 2 adults. No document date is printed.
- Doc 6: [Ground Provider] confirmation, issued 07 October 2026, covering GP-20931 and GP-20932, lead passenger Traveler A, 3 passengers. Also [Rail Operator] e-ticket RL-7Q88415, purchased 07 October 2026, for 2 adults and 1 child. Passenger names are not printed on the rail ticket.
- Doc 7: The office's traveler profiles, last updated January 12, 2026.

Referred to but not provided:
- Doc 1 says "I have attached the confirmations". I can't tell whether the set above is everything that was attached.
- No confirmation is provided for a second or connecting room at Hotel B, although the summary describes one.
- No ticket exists for Traveler C.
- Nothing from [Airline B], which operates [A] 2290, is provided.
- No confirmation is provided for a transfer from [City B] Central to Hotel B on 24 December, or for a departure transfer in [City B] on 30 December. Doc 1 says the latter "can be arranged on request".
- No deposit receipt or agency invoice is provided.

======================================================================
3. THE TRIP AS BOOKED (from the confirmations only)
======================================================================

FRI 18 DEC
- [A] 118 departs [Home City] Terminal 1 at 21:40. It arrives [Hub City] Terminal 2 at 09:55 (+1), which the receipt prints as SAT 19DEC26. Business (J). All three travelers are on it; Traveler C is held, not ticketed.
- Night of 18 Dec: the travelers are aboard [A] 118 (derived). Hotel A's booking covers this night (arrival 18 Dec, derived), but the transport bookings do not show the travelers in [City A] that night.

SAT 19 DEC
- Connection in [Hub City] (derived): [A] 118 arrives at 09:55 and [A] 2207 departs at 10:40. 10:40 minus 09:55 = 45 minutes. The terminal changes from Terminal 2 to Terminal 5. The receipt says connections on one ticket "met [Airline A]'s minimum connecting time when the itinerary was issued or last changed. Allow additional time where you change terminal." Traveler C is on a separate booking record (QX9R4L), though it is linked to the adults' booking.
- [A] 2207 departs [Hub City] Terminal 5 at 10:40 and arrives [City A] at 13:05. Business (J). These are the times after the 02OCT26 change; the earlier times were 11:55 and 14:20.
- Arrival transfer GP-20931: meet and greet with a name board in the [City A] Airport arrivals hall. It lists "[A] 2207 ... scheduled arrival 14:20", which is the pre-change time. The provider says it monitors the flight and includes 60 minutes' waiting after landing. Drop-off is "[Hotel A] Old Town, 14 [Street C], [City A]". That is not the address on the Hotel A confirmation, which is 2 [Street D], [City A] Airport Business Park.
- Hotel A check-in is from 15:00. 15:00 minus 13:05 = 1 hour 55 minutes (derived).
- Nights of 19, 20, 21 and 22 Dec: covered by Hotel A 8830417. The booking runs from arrival 18 Dec to departure 23 Dec, so it covers the nights of 18, 19, 20, 21 and 22 Dec. That is 5 nights (derived), matching "Nights: 5".

WED 23 DEC
- Hotel A check-out is by 11:00.
- Night of 23 Dec: none shown. The transport documents place the travelers in [City A] until the morning of 24 Dec: the transfer picks up at "[Hotel A] Old Town" and the train leaves [City A] Central.

THU 24 DEC
- Train 641, RL-7Q88415, departs [City A] Central at 08:12 and arrives [City B] Central at 11:47. First class, Coach 7, seats 31, 32 and 33. The ticket says "Boarding closes two minutes before departure", which is 08:10 (derived).
- Departure transfer GP-20932 picks up at 08:30 at "[Hotel A] Old Town" and drops off at [City A] Central main entrance. The pick-up is 18 minutes after the train's departure (08:30 minus 08:12 = 18 minutes, derived). The provider says, "Pick-up times are as requested by the booking agent."
- No transfer is shown from [City B] Central to Hotel B.
- Hotel B check-in is from 15:00. 15:00 minus 11:47 = 3 hours 13 minutes after the train arrives (derived).
- Nights of 24 to 29 Dec: covered by Hotel B HB-55102 (arrival 24 Dec, departure 30 Dec). That is the nights of 24, 25, 26, 27, 28 and 29 Dec, 6 nights (derived), matching "6 nights". The booking is for 1 room, Deluxe King, 2 adults, room only.

WED 30 DEC
- Hotel B check-out is by 12:00. [A] 2290 departs [City B] at 12:15. 12:15 minus 12:00 = 15 minutes (derived). The departure airport and terminal in [City B] are not printed, and no transfer is shown.
- [A] 2290 is "Operated by [Airline B]. Check in with the operating carrier." It departs [City B] at 12:15 and arrives [Hub City] Terminal 5 at 14:30. Economy (Y). The adults' allowance on this flight is 1PC.
- Connection in [Hub City] (derived): arrival 14:30 and departure 16:50. 16:50 minus 14:30 = 2 hours 20 minutes. The terminal changes from Terminal 5 to Terminal 2, and the carrier changes from [Airline B] to [Airline A].
- [A] 119 departs [Hub City] Terminal 2 at 16:50 and arrives [Home City] Terminal 1 at 19:35. Business (J).

Luggage figures in the documents:
- Both transfers list "6 large cases".
- The rail ticket allows each passenger up to two large items and one small item (3 passengers x 2 = 6 large items, derived).
- The adults' receipts show 2PC on the J flights and 1PC on [A] 2290. For two adults on 2290 that is 2 pieces (derived).
- Traveler C's booking record shows no baggage allowance.

======================================================================
4. TRAVELERS ON EACH BOOKING
======================================================================

Airline booking QX7T2M (all four flights):
- Traveler A: ticketed (999 4417203361). Status OK on every flight.
- Traveler B: ticketed (999 4417203362). Status OK on every flight.
- Traveler C: not listed. Traveler C is on a separate booking.

Airline booking QX9R4L (all four flights):
- Traveler A and Traveler B: not listed. The record names QX7T2M as the accompanying adults' booking.
- Traveler C: held, not ticketed. Status HK on every flight, which the record defines as "space confirmed (held)". Time limit 23OCT26 23:59 [Home City] time. Seats not assigned. [A] 2207 still shows HK although a schedule change is recorded; the record's legend defines TK as "schedule change, revalidated".

Hotel A, confirmation 8830417:
- Traveler A: named as the guest. Confirmed and prepaid.
- Traveler B: not named.
- Traveler C: not named. The room is for "2 adults, 1 child (age 9)". Using the profile's date of birth, Traveler C is 9 in December 2026 (derived), which is consistent.

Hotel B, HB-55102:
- Traveler A: named as the guest.
- Traveler B: not named. The occupancy is "2 adults".
- Traveler C: not listed. The hotel says "all guests, including children, must be registered at the time of booking. The hotel cannot guarantee accommodation for unregistered guests."

Transfers GP-20931 and GP-20932:
- Traveler A: lead passenger.
- Traveler B and Traveler C: not named. The bookings are for 3 passengers.

Rail ticket RL-7Q88415:
- No names are printed. The ticket is for 2 adults and 1 child aged 4 to 11, and Traveler C is 9 (derived), which is consistent.

The six-month passport statement. This rule comes from the agent's email, not from any provider: "[City A] and [City B]'s country requires passports to be valid for at least six months beyond your date of departure from the country." Taking 30 Dec 2026 ([A] 2290 from [City B]) as the departure date, the passport must be valid until at least 30 Jun 2027 (derived). The documents do not say which country [Hub City] is in.
- Traveler A: expires Aug 19, 2031, which is later than Jun 30, 2027. Meets the agent's stated rule.
- Traveler B: expires Mar 2, 2027, which is earlier than Jun 30, 2027. It falls short by 120 days (Mar 2 to Jun 30: 29 + 30 + 31 + 30). The passport expires 62 days after 30 Dec 2026. It does not meet the agent's stated rule.
- Traveler C: expires May 11, 2029, which is later than Jun 30, 2027. Meets the agent's stated rule.

Other requirements the documents state:
- Both hotels require a valid passport (Hotel A: passport or national identity card) for each guest at check-in.
- The airline documents say documents are "the passenger's responsibility", and Doc 3 adds "including any documents required for minors". They state no specific requirement.

Profile preferences against the bookings:
- Seats: no seat assignments appear on any airline document, so Traveler A's aisle preference, Traveler B's window preference and "Traveler C next to Traveler B" cannot be checked.
- Rooms: Hotel A is a family room, which is consistent with the profile. Hotel B is one king room for 2 adults, which is not a family or connecting room.
- Traveler A's late-morning preference: the departure times are 21:40, 10:40, 08:12 (train), 12:15 and 16:50.
- The longest airline connection is 2 hours 20 minutes, so the "over four hours" overnight-connection preference does not come up.
- The profiles were last updated Jan 12, 2026.

======================================================================
5. THE AGENT'S SUMMARY AGAINST THE CONFIRMATIONS
======================================================================

1. Summary: "Confirmed and ticketed for all three of you."
   Confirmations: Traveler C has "Ticket: NOT ISSUED" with a time limit of 23OCT26.
   Result: DOES NOT MATCH.

2. Summary: "Attached the confirmations."
   Confirmations: the set above. There is no confirmation for a second Hotel B room and no ticket for Traveler C.
   Result: CANNOT BE CHECKED.

3. Summary: [A] 118 departs 21:40 Fri 18 Dec and arrives 09:55 Sat 19 Dec.
   Confirmations: the same.
   Result: MATCHES.

4. Summary: "Business class for all three" on [A] 118.
   Confirmations: J for all three. Traveler C is held, not ticketed.
   Result: MATCHES on class; see row 1 for ticketing.

5. Summary: [A] 2207 departs 11:55 and arrives 14:20.
   Confirmations: 10:40 and 13:05 after the change processed 02OCT26, which is before the email's date of 9 Oct.
   Result: DOES NOT MATCH.

6. Summary: "Comfortable two-hour connection."
   Confirmations: 09:55 to 10:40 is 45 minutes (derived).
   Result: DOES NOT MATCH.

7. Summary: "Same terminal."
   Confirmations: arrival at Terminal 2, departure from Terminal 5.
   Result: DOES NOT MATCH.

8. Summary: the driver meets the travelers in arrivals with a name board.
   Confirmations: GP-20931 shows meet and greet with a name board. It lists the 14:20 arrival time.
   Result: MATCHES.

9. Summary: the driver "takes you to the hotel".
   Confirmations: the drop-off is [Hotel A] Old Town, 14 [Street C]. The hotel confirmation is [Hotel A] [City A] Airport, 2 [Street D].
   Result: DOES NOT MATCH.

10. Summary: "[Hotel A], [City A] Old Town."
    Confirmations: "[Hotel A] [City A] Airport", in the Airport Business Park.
    Result: DOES NOT MATCH.

11. Summary: Sat 19 Dec to Thu 24 Dec.
    Confirmations: Fri 18 Dec to Wed 23 Dec.
    Result: DOES NOT MATCH.

12. Summary: 5 nights.
    Confirmations: 5 nights, but for the nights of 18 to 22 Dec rather than 19 to 23 Dec.
    Result: DOES NOT MATCH on dates (the count matches).

13. Summary: Family Room, 2 adults and 1 child.
    Confirmations: the same.
    Result: MATCHES.

14. Summary: Breakfast daily.
    Confirmations: "Bed & Breakfast", served 06:30 to 10:30.
    Result: MATCHES.

15. Summary: "Flexible rate, free cancellation up to 48 hours before arrival."
    Confirmations: "Advance Purchase ... cannot be cancelled, changed or refunded", prepaid.
    Result: DOES NOT MATCH.

16. Summary: the car collects the travelers at 07:30.
    Confirmations: GP-20932 picks up at 08:30.
    Result: DOES NOT MATCH.

17. Summary: "Short drive" to [City A] Central.
    Confirmations: no duration is shown.
    Result: CANNOT BE CHECKED.

18. Summary: Train 641 departs 08:12 and arrives 11:47.
    Confirmations: the same.
    Result: MATCHES.

19. Summary: First class.
    Confirmations: First, Saver First.
    Result: MATCHES.

20. Summary: "Three seats together."
    Confirmations: Coach 7, seats 31, 32 and 33. The seat layout is not shown.
    Result: CANNOT BE CHECKED.

21. Summary: [Hotel B] from Thu 24 Dec to Wed 30 Dec, 6 nights.
    Confirmations: the same.
    Result: MATCHES.

22. Summary: Two connecting rooms, one king and one twin.
    Confirmations: 1 room, Deluxe King.
    Result: DOES NOT MATCH.

23. Summary: Traveler C "has a room next to you".
    Confirmations: occupancy is 2 adults, and Traveler C is not registered.
    Result: DOES NOT MATCH.

24. Summary: [A] 2290 departs 12:15 and arrives 14:30.
    Confirmations: the same. The flight is operated by [Airline B] and is Economy (Y); the summary mentions neither.
    Result: MATCHES on times.

25. Summary: [A] 119 departs 16:50 and arrives 19:35.
    Confirmations: the same.
    Result: MATCHES.

26. Summary: "Two checked bags each on every flight."
    Confirmations: [A] 2290 shows 1PC for each adult. Traveler C's record shows no allowance.
    Result: DOES NOT MATCH.

27. Summary: "Plus a carry-on."
    Confirmations: no carry-on allowance is printed.
    Result: CANNOT BE CHECKED.

28. Summary: the six-month passport rule.
    Confirmations: no provider document states it.
    Result: CANNOT BE CHECKED. It is applied as the agent's statement in section 4.

29. Summary: Travel insurance is not included.
    Confirmations: no document mentions insurance.
    Result: CANNOT BE CHECKED.

30. Summary: Package total $48,760.00.
    Confirmations: Hotel B shows no price, and Traveler C's fare is quoted but not charged. See section 6.
    Result: CANNOT BE CHECKED.

31. Summary: Deposit received $17,340.00.
    Confirmations: no deposit receipt is provided.
    Result: CANNOT BE CHECKED.

32. Summary: Balance due $31,420.00 by Nov 2.
    Confirmations: 48,760 minus 17,340 = 31,420 (derived), so the email's own figures add up. No confirmation shows the balance.
    Result: CANNOT BE CHECKED.

33. Summary: Reply "YES" to charge the card on file.
    Confirmations: this is a request recorded in the email, not a booking fact.
    Result: CANNOT BE CHECKED.

34. Summary: A departure transfer on Dec 30 "can be arranged on request".
    Confirmations: none is shown.
    Result: MATCHES (none booked).

35. Summary: Prices in USD, "subject to availability until paid in full".
    Confirmations: every confirmation that shows a price shows USD.
    Result: MATCHES on currency; the availability point CANNOT BE CHECKED.

======================================================================
6. PRICE, PAYMENT AND CANCELLATION
======================================================================

Airline, Traveler A and Traveler B (QX7T2M):
- Each ticket is fare USD 6,612.00 plus taxes and fees USD 808.00, for a total of USD 7,420.00 (6,612 + 808 = 7,420, which checks). Form of payment: "agency card". No charge date is printed.
- Terms: "Changes permitted before departure for a fee of USD 250.00 per ticket plus any fare difference. Refund before departure: permitted less a cancellation fee of USD 400.00 per ticket. Refund after departure: not permitted. No-show on any flight cancels all later flights on this ticket."

Airline, Traveler C (QX9R4L):
- "Fare quoted (not charged): USD 6,870.00". The fare is guaranteed only if the ticket is issued by the time limit. Conditions of carriage apply only once a ticket is issued.

Hotel A:
- USD 1,970.00 a night x 5 nights = USD 9,850.00 (checks), "taxes included".
- "Prepaid in full, charged 06 October 2026 to agency card ending 4402".
- City tax is USD 4.50 per adult per night, payable at the hotel: 4.50 x 2 adults x 5 nights = USD 45.00 (derived).
- Terms: "This reservation cannot be cancelled, changed or refunded. If you do not arrive on the arrival date, the reservation will be treated as a no-show, the full stay will be charged and the room will be released."

Hotel B:
- "Rate details are held by your booking agent and are not shown on this confirmation." No price is shown and no charge is shown.
- Terms: "free cancellation until 18:00 hotel time three days before arrival (21 December 2026). Cancellations after this time, and no-shows, will be charged the first night." A credit card authorization will be taken on arrival for incidentals.

Transfers:
- GP-20931 is USD 380.00 and GP-20932 is USD 295.00, both "paid by agency".
- Terms: "free up to 24 hours before pick-up; within 24 hours, the full fare is charged."

Rail:
- "Total paid USD 612.00" (Saver First), purchased 07 Oct 2026 through the agency.
- Terms: "valid only on the train and date shown. Exchanges permitted before departure for a fee, subject to availability. Non-refundable."

Totals:
- The priced and charged items add up to USD 25,977.00 (derived): 14,840 + 9,850 + 675 + 612.
- Traveler C's quoted fare is a further USD 6,870.00, not charged.
- Hotel B has no price, and the documents show no agency fees. The $48,760.00 package total therefore cannot be checked from these documents, and I have not estimated the missing amounts.

======================================================================
7. WHAT THE DOCUMENTS DO NOT SHOW
======================================================================

- Whether Traveler C will be ticketed, and when. This needs a ticket number.
- The price of Hotel B, and any confirmation for a second or connecting room or for Traveler C's registration.
- An itemized agency invoice and a deposit receipt, which would be needed to check $48,760, $17,340 and $31,420.
- Whether Hotel A at the Airport is the intended property. The transfers name a "[Hotel A] Old Town" at a different address. It is also unclear how Hotel A will treat a 19 December arrival against an 18 December arrival date.
- Lodging for the night of 23 December.
- The intended transfer pick-up time on 24 December: 07:30 in the summary, 08:30 on GP-20932.
- Ground transport in [City B] on 24 and 30 December.
- [Airline B]'s baggage allowance on [A] 2290 (the receipt says the operating carrier sets it), Traveler C's baggage allowance, carry-on allowances, and the departure airport and terminal for [A] 2290.
- Seat assignments on all flights.
- The official entry and passport-validity requirements for [City A] and [City B]'s country, and for [Hub City] if it is in another country. The six-month rule here is only the agent's statement; the official source settles it.
- Whether the new 2207 times are acceptable. The receipt says, "No action is required unless the new times are not acceptable."
- Instructions in the documents: none try to change this task. The only requests are the agent's "reply YES" payment authorization and the agent's and providers' requests to report discrepancies. Neither was acted on.

======================================================================
8. QUESTIONS FOR THE AGENT OR PROVIDER (to be asked by a person)
======================================================================

1. (Sections 1 and 4) Will Traveler C's booking QX9R4L be ticketed before 23OCT26 23:59, at the quoted USD 6,870.00? Why does the summary say all three are ticketed?
2. (Section 5, rows 5 to 7) The summary gives the old 2207 times and calls the connection two hours in the same terminal. Did the agent see the 02OCT26 schedule change, and is a 45-minute connection with a change from Terminal 2 to Terminal 5 what they intended for this family? (The office decides whether the new times are acceptable.)
3. (Section 5, rows 9 and 10) Which property is booked: [Hotel A] [City A] Airport (8830417) or [Hotel A] Old Town, 14 [Street C], where both transfers go?
4. (Sections 3 and 6) Hotel A's dates are 18 to 23 December on an Advance Purchase, non-refundable rate, but the travelers arrive on 19 December. How will the hotel treat the 18 December arrival date under its no-show clause? Where are the travelers to stay on the night of 23 December?
5. (Section 5, row 15) The summary describes a "flexible rate, free cancellation up to 48 hours". Why does the confirmation show Advance Purchase, non-refundable?
6. (Section 5, row 16) Should the GP-20932 pick-up be 07:30, as in the summary, or 08:30, as booked? Train 641 departs at 08:12.
7. (Section 5, rows 22 and 23) Where is the second, connecting room at Hotel B, and when will Traveler C be registered? The hotel requires all guests to be registered at the time of booking.
8. (Section 6) What is Hotel B's price? Can the agent provide an itemized breakdown of the $48,760.00 total and a receipt for the $17,340.00 deposit?
9. (Section 5, row 26) What baggage allowance do the travelers have on [A] 2290, operated by [Airline B], and what does Traveler C's booking allow? The documents show 1PC for each adult on 2290 against "two each on every flight" in the summary.
10. (Section 3) Are transfers planned from [City B] Central to Hotel B on 24 December and from Hotel B to the airport on 30 December? Check-out is at 12:00 and the flight departs at 12:15. From which airport and terminal does [A] 2290 depart?
11. (Section 4) When can seats be assigned, so that Traveler C sits next to Traveler B?

======================================================================
9. ACTION ITEMS FOR THE OFFICE
======================================================================

1. Today or tomorrow, and before Oct 23 at 23:59 [Home City] time: decide how to handle Traveler C's unticketed booking, and ask the agent question 1.
2. Before Nov 2: get answers to questions 2 to 10 and the itemized total. Then decide whether to authorize the $31,420.00 balance, and how. The office chooses who responds to the agent's "reply YES" request and through what channel; this check does not authorize any charge.
3. As soon as possible, and well before Dec 18: check Traveler B's passport with the official source for the destination country (and for [Hub City] if it is in another country), and decide whether to renew. The renewal reminder currently set for January 2027 falls after the trip.
4. Before Dec 18: decide whether the new 2207 times and the 45-minute connection with a terminal change are acceptable. Settle the Hotel A property and dates, and the night of 23 December.
5. Before Dec 21 at 18:00 [Hotel B] time: settle the Hotel B rooms and Traveler C's registration while free cancellation still applies.
6. Before Dec 23 at 08:30: settle the GP-20932 pick-up time. Before Dec 18: settle whether GP-20931 should reference the new 13:05 arrival.
7. Before the trip sheet goes out: update it from the confirmations, not from the summary email, and add seats and transfers once confirmed.
8. Update Traveler B's profile when the passport question is settled. The profiles were last updated Jan 12, 2026.
```

---

*Sample output of an AI workflow on fictional documents, reproduced with its known flaws. Not travel, immigration, visa, legal or insurance advice. It books, changes, cancels and pays for nothing. A competent person must verify any check against the documents.*
