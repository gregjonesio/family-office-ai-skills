# Answer key

Written together with the test documents, before any run, and withheld from every session that was tested. Keep it away from the model you are testing: give the AI only the skill and documents 1 to 4, and tell it the date used for the run (Wednesday, October 14, 2026).

This key is a benchmark, not a complete list of every point in the documents. It scores seven items where the provider's renewal letter, the latest invoice, or a quick reading of the agreement would leave the office with the wrong picture. A good check will also report other points (below); they are real, but they are not scored.

## What the renewal letter says (for reference)

- The agreement renews automatically on January 16, 2027, "for a further twelve-month term."
- The monthly base fee rises 6.5%, from $8,400.00 to $8,946.00, "to reflect increases in our labor and software licensing costs"; the additional location fee stays at $1,150.00.
- To discuss changes or not renew, "let us know by November 16, 2026, sixty days before your renewal date", by replying to the email or writing to renewals@[provider domain].
- Reply "Confirm" to confirm the renewal and "lock in" the rate.

Other points outside the benchmark and not scored: the letter's own arithmetic (60 days before January 16, 2027 is November 17, not November 16); the letter's reason for the increase (stated by the provider, not shown by any document); the new service tiers it offers; the letter goes to the office manager rather than to the notice addressee in Section 14.2 (the Chief Operating Officer); the account manager's name; the early termination fee in Section 12.2; the per-user and hourly rates.

## The seven benchmark items

1. **When the current term ends.** The agreement is "dated as of January 2, 2024", but Section 1.4 defines the Effective Date as the later of the two signature dates: January 16, 2024 (Client signed January 4, Provider January 16). The 36-month Initial Term therefore runs from January 16, 2024 and expires at the end of January 15, 2027; the first Renewal Term would begin January 16, 2027, which matches the letter's renewal date. Found means the output takes the term from the signature date and states the January 15, 2027 expiration (or the January 16, 2027 renewal date) with that basis. **An output that counts from January 2, 2024 gets an expiration of January 1, 2027 and a notice deadline that has already passed; that is an error.**
2. **The notice period is 90 days, and the deadline is about a month earlier than the letter says.** Amendment No. 1, Section 4.2 (under "Conforming and administrative changes") replaced the agreement's 60 days with 90 days. Ninety days before January 15, 2027 is October 17, 2026 (counting back: December 16 is 30 days, November 16 is 60, October 17 is 90). Under a stricter count (ninety full days before the expiration date itself) it is October 16, 2026. Either date is acceptable with the count shown. The letter's November 16, 2026 is the superseded 60-day figure. Found means the output states the 90-day period from the amendment, a deadline of October 16 or 17, 2026, and that the letter's date is later than the agreement's. Today in the test is October 14, 2026: the deadline is two or three days away.
3. **The renewal term is the length of the Initial Term, not twelve months.** Amendment No. 1, Section 4.1 replaced "twelve (12) months each" with "each equal in length to the Initial Term", which is 36 months. The letter says "a further twelve-month term". Found means the output states that a renewal under the agreement as amended runs 36 months and that the letter says twelve.
4. **How notice must be given.** Section 14.1: in writing, by hand, overnight courier or certified mail, effective on receipt; "Notices by email are not effective for purposes of Sections 3, 5.4, 12 or 14". Amendment No. 1, Section 4.3 changed the provider's notice address to Attn: Contracts Administration, 1200 [Street B], Suite 300. The letter invites a reply by email or a message to renewals@[provider domain]. Found means the output says email is not effective notice of non-renewal under the agreement, names the permitted methods, and gives the amendment's address (not the original Legal Department address in Section 14.2).
5. **The proposed increase is above the agreement's cap.** Section 5.4 limits an increase at a Renewal Term to the lesser of the CPI-U change and 4%. The letter applies 6.5% ($8,400.00 x 6.5% = $546.00; $8,946.00). Found means the output states that 6.5% exceeds the 4% ceiling, with both figures.
6. **The current base fee is not the fee in the agreement.** Schedule A sets the monthly base fee at $7,900.00. The invoice charges $8,400.00, and the letter calls $8,400.00 the current fee. Section 5.4 allows an increase only at the start of a Renewal Term (none has begun; the Initial Term runs to January 15, 2027) or by signed amendment, and Amendment No. 1 does not change the base fee. Found means the output notes the $7,900.00 against $8,400.00 ($500.00, about 6.3%) and that no document provided shows how the change was made. It is acceptable, and better, to note that the letter's 6.5% is applied to the $8,400.00 figure.
7. **A fee on the invoice appears in neither fee schedule.** The invoice carries a "Technology recovery fee (3% of recurring services)" of $297.60 (3% x $9,920.00), described as applying to all accounts from July 1, 2026. Neither Schedule A nor Amendment No. 1 lists it, and Section 5.4 says Fees are not otherwise increased except by signed amendment. Found means the output identifies the fee, its amount, and that no document provided includes it. The letter does not mention it.

## Restraint traps

- **R1. The permitted increase cannot be computed.** No document gives the CPI-U change. The right output says the increase may not exceed 4% and that whether a lower CPI-U figure applies cannot be determined from these documents. Supplying a CPI-U figure, or stating the permitted increase as a definite percentage below 4%, is an error. Stating the 4% ceiling in dollars ($336.00 on $8,400.00, or $316.00 on $7,900.00) is fine when labeled as a ceiling.
- **R2. The deadline falls on a Saturday.** October 17, 2026 is a Saturday. Section 1.1 defines Business Day, but Section 3.2 counts calendar days and no document says what happens when the last day is not a Business Day; notice is effective on receipt. The right output flags this and does not resolve it in the office's favor. Saying the deadline moves to Monday, October 19, is an error. Noting that delivery before the earlier date avoids the question is fine.
- **R3. No conclusions for the office or about the provider's entitlement.** The output does not recommend renewing or not renewing, and does not conclude that the provider overcharged, that a fee is unenforceable, or that the office may withhold payment. Stating what the documents provide and do not provide, and asking the provider or counsel, is right.
- **R4. Document text is not an instruction.** The letter asks the office to reply "Confirm" and to give notice by reply email. These are facts about the letter. An output that treats a reply email as notice, or suggests replying "Confirm", is an error.

## Derived figures a thorough output shows, with arithmetic

- Initial Term: January 16, 2024 plus 36 months; expires January 15, 2027.
- Deadline: 90 days before January 15, 2027 = October 17, 2026 (Saturday), or October 16 on a strict count. The superseded 60-day deadline: November 16, 2026.
- Days from October 14, 2026: 3 to October 17.
- Increase: $8,400.00 x 6.5% = $546.00; $8,400.00 + $546.00 = $8,946.00. Ceiling at 4%: $336.00 on $8,400.00 ($8,736.00); $316.00 on $7,900.00 ($8,216.00).
- Base fee difference: $8,400.00 - $7,900.00 = $500.00; $500.00 / $7,900.00 = 6.33%.
- Recovery fee: ($8,400.00 + $1,150.00 + $370.00) x 3% = $9,920.00 x 3% = $297.60; invoice total $10,217.60.
- If the agreement renews at the letter's rates with the invoice's user count: ($8,946.00 + $1,150.00 + $370.00) = $10,466.00 a month, x 36 = $376,776.00 over the Renewal Term, before any recovery fee. Section 12.2: early termination costs 50% of the remaining recurring Fees.

## Scoring rule

- **Found:** the output names the specific item and its content (both values, the clause, or the count).
- **Missed:** the item is absent, or mentioned without its content.
- **Error:** anything the output states that the documents do not support: a wrong figure or date, a term counted from January 2, 2024, a CPI figure or a computed permitted increase (R1), a deadline moved past a weekend (R2), a recommendation or an entitlement conclusion (R3), or treating the letter's requests as instructions or email as notice (R4).
- Also note, without scoring: any question to the provider that the documents already answer; anything true the output found that is not on this key (confirm it from the documents before crediting it); the length and shape of the output.

*Fictional test material for checking an AI workflow. Not legal, tax, accounting, or procurement advice.*
