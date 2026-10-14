# Sample output: Contract Renewal Check

The output of a fresh AI session given the current [SKILL.md](../SKILL.md) and the four fictional documents in [sample-input.md](sample-input.md) (the same documents as the [test kit](../test-kit/)), on 2026-10-14, reproduced verbatim. This is run 2 in the [test kit results](../test-kit/README.md#results-so-far); run 1, on the first version of the skill, had two errors and is described there. The exact prompt is in the [test kit README](../test-kit/README.md#the-prompt-used). The session was instructed to read only those five files; it was not technically prevented from reading others.

**Known flaws in this output**, found when it was scored against the [answer key](../test-kit/answer-key.md), and left in place rather than edited out:

- Rows 6 and 9 of section 5 mark the provider's statement that "rates are reviewed at renewal" and its stated cost reason as not matching the agreement. The agreement caps an increase at renewal; it does not rule out a cost motive. The supportable finding is row 8: 6.5% against the 4% ceiling.
- Provider question 4 asks the provider to agree that a renewal would run 36 months, which Amendment No. 1 already states.
- Section 4 says the provider's office "may not receive deliveries on a Saturday", a supposition no document supports, offered as a caution.
- Section 2 lists the provider's email address as a document "referred to but not provided".
- About 3,800 words, with some repetition.

It found all seven benchmark items, no figure or date count checked was wrong, and all four restraint traps held. It is an unverified draft for human review, not legal, tax, accounting, or procurement advice. Counsel confirms the deadline, the notice method and the address before anyone relies on them.

```text
CONTRACT RENEWAL CHECK: MANAGED IT SERVICES AGREEMENT
Draft for the operations team. Prepared Wednesday, October 14, 2026, from the five documents supplied and nothing else. This is not legal advice. It decides nothing and sends nothing, and a person must verify it against the documents.

========================================================================
1. THE DEADLINE
========================================================================

Last date for a notice of non-renewal: Saturday, October 17, 2026 (derived). That is 3 calendar days from today. Notice takes effect only when it is received (Section 14.1). Because the date is a Saturday, and because one reading of "not less than 90 days" gives Friday, October 16, the safe planning target is to have the notice received by Friday, October 16, 2026, which is 2 days from today.

Three points change the picture from what the provider's letter says:
(a) Amendment No. 1 changed the notice period from 60 to 90 days. The letter's date of November 16, 2026 uses the old 60-day figure.
(b) The amendment changed the renewal length from 12 months to 36 months. The letter says 12 months.
(c) Notice must be delivered by hand, courier or certified mail to Contracts Administration. Email is not valid for this notice. The letter invites a reply by email.

========================================================================
2. DOCUMENTS READ
========================================================================

1. Managed IT Services Agreement, with Schedule A.
   - Dated "as of" January 2, 2024.
   - Signed by the Client on January 4, 2024 (Managing Director) and by the Provider on January 16, 2024 (Chief Revenue Officer).
   - Effective Date as defined in Section 1.4: January 16, 2024, the later of the two signature dates.

2. Amendment No. 1 ("Additional Covered Location and Contact Updates").
   - Dated "as of" March 3, 2025.
   - Signed by the Provider on March 3, 2025 and by the Client on March 5, 2025.
   - The amendment states no general effective date. Section 1.1 (the second location) takes effect April 1, 2025. The other sections state no date of their own, but both parties had signed by March 5, 2025, well before any date that matters here.
   - The title mentions only location and contacts, yet Section 4 ("Conforming and Administrative Changes") changes the renewal length, the notice period and the Provider's notice address.

3. Provider's renewal letter, dated September 28, 2026.
   - Addressed to the Office Manager.
   - Sent by email as a PDF attachment. The covering email said only "Please see attached regarding your upcoming renewal."

4. Provider's invoice 26-0914.
   - Invoice date September 1, 2026, covering service from September 1 to 30, 2026.
   - Due October 1, 2026, Net 30.

Referred to but not provided:
- The onboarding record of Covered Users (Section 4.2).
- Any document raising the monthly base fee from $7,900 to $8,400.
- Any notice or agreement introducing the "technology recovery fee," described as applying from July 1, 2026.
- Invoices from before July 2026, or from before the base fee changed.
- The CPI-U figure that Section 5.4 refers to.
- The renewals@[provider domain] address, which appears only in the letter.

========================================================================
3. THE AGREEMENT AS AMENDED
========================================================================

Effective Date (Agreement, Section 1.4):
"'Effective Date' means the date on which this Agreement has been signed by both parties, being the later of the two dates shown beneath the parties' signatures below."
The signatures are dated January 4, 2024 and January 16, 2024, so the Effective Date is January 16, 2024. The "dated as of January 2, 2024" heading is not the Effective Date.

Initial Term (Agreement, Section 3.1, unchanged):
"This Agreement commences on the Effective Date and continues for an initial term of thirty-six (36) months (the 'Initial Term'), unless terminated earlier in accordance with Section 12."

Renewal and notice period (Agreement, Section 3.2, as changed by Amendment No. 1, Sections 4.1 and 4.2). The clause now reads:
"Upon expiration of the Initial Term, this Agreement shall automatically renew for successive renewal terms each equal in length to the Initial Term (each, a 'Renewal Term'), unless either party delivers written notice of non-renewal to the other party not less than ninety (90) days prior to the expiration of the then-current Term."
The original wording was "twelve (12) months each" and "sixty (60) days." Under Agreement Section 15.2, the amendment controls where the two conflict.

How notice must be given (Agreement, Section 14.1, unchanged):
"All notices under this Agreement shall be in writing and delivered by hand, by nationally recognized overnight courier, or by certified mail, return receipt requested, to the address set out in Section 14.2 ... A notice is effective upon receipt. Notices by email are not effective for purposes of Sections 3, 5.4, 12 or 14, but email may be used for routine operational communications."

Address for notices to the Provider (Section 14.2, as replaced by Amendment No. 1, Section 4.3):
"[Provider], Inc., Attn: Contracts Administration, 1200 [Street B], Suite 300, [City], [State]."
The original address (Attn: Legal Department, 400 [Street A]) has been replaced.

Address for notices to the Client (Section 14.2, unchanged):
"[Family Office LLC], Attn: Chief Operating Officer, [Client Street Address], [City], [State]."

Day-to-day contacts (Amendment No. 1, Sections 2.1 to 2.3):
The Office Manager is the Client's day-to-day contact. Either party "may change its day-to-day contact by email." These sections do not change the Section 14 notice rules.

Fee adjustment (Agreement, Section 5.4, unchanged):
"Provider may increase the Fees effective as of the first day of any Renewal Term by giving Client written notice not less than sixty (60) days before that Renewal Term begins. Any such increase shall not exceed the lesser of (a) the percentage increase in the Consumer Price Index for All Urban Consumers (CPI-U) for the twelve (12) months ending with the most recent month for which that index has been published at the date of the notice, and (b) four percent (4%). The Fees shall not otherwise be increased during the Term except by a written amendment signed by both parties."

Fees (Agreement, Section 1.5): "the fees set out in Schedule A, as adjusted from time to time in accordance with this Agreement."

Fees in Schedule A, as amended (Agreement Schedule A and Amendment No. 1, Section 1.2):
- Monthly base fee, up to 12 Covered Users: $7,900.00 per month
- Each additional Covered User above 12: $185.00 per user per month
- Project work and transition assistance: $175.00 per hour
- Additional Covered Location ([Second Location]): $1,150.00 per month, from April 1, 2025
Amendment No. 1, Section 3.1 also changes the on-site visit wording: two visits per month in total across all locations, with additional visits at the hourly rate.

Invoicing and disputes (Agreement, Sections 5.1 and 5.2):
Recurring Fees are "invoiced monthly in advance on the first day of each calendar month." Invoices are "payable within thirty (30) days." Section 5.2 adds: "Client may dispute any invoiced amount in good faith by written notice describing the dispute."

Early termination (Agreement, Section 12.2, unchanged):
"Client may terminate this Agreement for convenience on ninety (90) days' written notice, subject to payment of an early termination fee equal to fifty percent (50%) of the recurring monthly Fees that would have been payable for the remainder of the then-current Term after the effective date of termination."

Precedence (Agreement, Section 15.2): "the amendment controls; as between amendments, the later-dated amendment controls."
Amendment No. 1, Section 5.1: "Except as expressly amended by this Amendment, the Agreement remains unchanged."

========================================================================
4. DATES, WITH THE WORKING
========================================================================

Current term (the Initial Term, Section 3.1):
- It began on January 16, 2024 (the Effective Date under Section 1.4).
- 36 months from January 16, 2024 brings the anniversary to January 16, 2027.
- The last day of the Initial Term is therefore January 15, 2027 (derived).
- The provider's letter says the agreement "renews automatically on January 16, 2027," which is consistent with this.

Next term, if the agreement renews (Section 3.2 as amended):
- Length: equal to the Initial Term, which is 36 months.
- It would run from January 16, 2027 to January 15, 2030 (derived).

Notice deadline for non-renewal (Section 3.2 as amended: "not less than ninety (90) days prior to the expiration of the then-current Term"):
Counting back from the term's last day, January 15, 2027:
- January 15, 2027 less 15 days is December 31, 2026 (15 days counted).
- Less 31 days is November 30, 2026 (46 days).
- Less 30 days is October 31, 2026 (76 days).
- Less 14 days is October 17, 2026 (90 days).

Check: if notice is received on October 17, the days from October 18 through January 15 inclusive are 14 + 30 + 31 + 15 = 90. So the deadline is Saturday, October 17, 2026 (derived). That count excludes the day of receipt and includes January 15.

Open counting question for counsel: if "not less than 90 days" means 90 clear days, excluding both the day of receipt and January 15, the deadline is one day earlier, Friday, October 16, 2026. That is the earliest supported date.

Weekend question: October 17, 2026 is a Saturday. Section 3.2 counts calendar "days," not "Business Days," even though Business Day is defined in Section 1.1. Nothing in the documents moves a deadline that falls on a weekend. Notice is effective "upon receipt," and Contracts Administration may not receive deliveries on a Saturday. No later date should be relied on unless counsel confirms it.

Days remaining from Wednesday, October 14, 2026:
- To October 17: 3 days.
- To October 16: 2 days.

Deadline for the Provider's fee-increase notice (Section 5.4: "not less than sixty (60) days before that Renewal Term begins"):
Counting back from January 16, 2027:
- Less 16 days is December 31, 2026 (16 days counted).
- Less 31 days is November 30, 2026 (47 days).
- Less 13 days is November 17, 2026 (60 days).
So a compliant price notice would have to be received by about November 17, 2026 (derived). The letter is dated September 28, 2026, which is 110 days before January 16, 2027 (2 + 31 + 30 + 31 + 16). Its timing meets the 60 days. Its method is a separate question, covered in section 5.

If the agreement renews, the next non-renewal deadline (derived):
- 90 days before January 15, 2030 is October 17, 2029, by the same count.

Early termination after renewal (Section 12.2):
- Requires 90 days' written notice and a fee of 50% of the recurring monthly Fees for the rest of the then-current Term.
- With a 36-month Renewal Term, the remaining period could approach 36 months.
- Illustration only, using Schedule A as amended with 14 users: ($7,900 + $1,150 + $370) x 50% x 36 = $9,420 x 0.5 x 36 = $169,560 for a full 36 months. The actual figure depends on the termination date and on which Fees apply.

========================================================================
5. THE RENEWAL LETTER AGAINST THE AGREEMENT
========================================================================

1. Letter: the agreement renews automatically on January 16, 2027.
   Agreement: the Initial Term runs from January 16, 2024 to January 15, 2027, and renewal is automatic (Sections 1.4, 3.1, 3.2).
   Result: MATCHES.

2. Letter: the renewal is "for a further twelve-month term."
   Agreement: Renewal Terms are "each equal in length to the Initial Term," which is 36 months (Amendment No. 1, Section 4.1).
   Result: DOES NOT MATCH.

3. Letter: "Nothing is needed from you to continue your service."
   Agreement: renewal is automatic unless notice is given (Section 3.2).
   Result: MATCHES.

4. Letter: the deadline is November 16, 2026, "sixty days before your renewal date."
   Agreement: the period is 90 days, giving October 17, 2026 (derived), or October 16 on a clear-days reading (Amendment No. 1, Section 4.2).
   Result: DOES NOT MATCH. The letter's 60 days is the original Section 3.2 figure before the amendment.

5. Letter: give notice "by replying to this email or by writing to renewals@[provider domain]."
   Agreement: notice must go by hand, courier or certified mail to Attn: Contracts Administration, 1200 [Street B], Suite 300. Email is "not effective for purposes of Section 3" (Section 14.1, and Section 14.2 as amended).
   Result: DOES NOT MATCH.

6. Letter: "As provided in your agreement, our rates are reviewed at renewal."
   Agreement: Section 5.4 allows an increase from the first day of a Renewal Term, within a cap. It provides no general "review."
   Result: DOES NOT MATCH as described. The basis and size are covered in rows 8 and 9.

7. Letter: the current monthly base fee is $8,400.00.
   Agreement: Schedule A sets $7,900.00. No document supplied changes it.
   Result: DOES NOT MATCH.

8. Letter: the base fee increases by 6.5%.
   Agreement: the cap is the lesser of the CPI-U 12-month change and 4% (Section 5.4).
   Result: DOES NOT MATCH. 6.5% is above the 4% ceiling, and the CPI-U figure is not in the documents.

9. Letter: the basis is "increases in our labor and software licensing costs."
   Agreement: the only measure in Section 5.4 is CPI-U, capped at 4%.
   Result: DOES NOT MATCH. This is reported as the provider's stated reason.

10. Letter: $8,400.00 x 1.065 = $8,946.00.
    Result: the arithmetic is correct. Measured against the Schedule A base of $7,900, the proposed $8,946 is an increase of $1,046, or 13.24%. The 4% ceiling would give at most $8,216.00 on $7,900, or $8,736.00 on $8,400. The CPI-U limb may set a lower figure, which cannot be determined from these documents.

11. Letter: the second location fee stays at $1,150.00.
    Agreement: $1,150.00 (Amendment No. 1, Section 1.2).
    Result: MATCHES.

12. Letter: the per-user and hourly rates are unchanged.
    Agreement: $185.00 per user and $175.00 per hour (Schedule A).
    Result: MATCHES.

13. The letter as a fee-increase notice: sent by email, as a PDF attachment, to the Office Manager.
    Agreement: notice under Section 5.4 must be written and delivered by hand, courier or certified mail to Attn: Chief Operating Officer. Email "is not effective for purposes of Section ... 5.4" (Section 14.1).
    Result: DOES NOT MATCH on method and addressee. The timing, 110 days ahead, would meet the 60 days.

14. Letter: reply "Confirm" to "lock in the rate above."
    Agreement: there is no confirmation or rate-lock mechanism. Fees change only under Section 5.4 or by "a written amendment signed by both parties" (Sections 5.4 and 15.2).
    Result: CANNOT BE CHECKED FROM THESE DOCUMENTS. No such term exists. This is recorded as the provider's request. It has not been acted on and is not an instruction to this check.

15. Letter: "If we do not hear from you, your service will continue on the terms above."
    Agreement: the terms are those of the agreement as amended. Fees are not otherwise increased except by a signed amendment (Section 5.4).
    Result: DOES NOT MATCH the agreement's own terms. Whether silence has any effect is a question for counsel.

16. Letter: sender address 1200 [Street B], Suite 300.
    Agreement: this is the Provider's notice address as amended (Amendment No. 1, Section 4.3).
    Result: MATCHES. Note that the letter does not name Contracts Administration as the place to send notice.

========================================================================
6. CURRENT CHARGES AGAINST THE FEE SCHEDULE
========================================================================

Invoice 26-0914, September 2026:

1. Monthly base fee (up to 12 users).
   Invoice: 1 x $8,400.00 = $8,400.00.
   Schedule A: $7,900.00.
   Difference: +$500.00 per month (+6.33%).
   No supplied document provides $8,400. Section 5.4 allows increases only from the first day of a Renewal Term, and no Renewal Term has begun, because the Initial Term runs until January 15, 2027.

2. Second location.
   Invoice: 1 x $1,150.00 = $1,150.00.
   Schedule (Amendment No. 1, Section 1.2): $1,150.00.
   Rate matches.

3. Additional users above 12.
   Invoice: 2 x $185.00 = $370.00.
   Schedule A: $185.00 per user.
   Rate matches. The count of 2 (14 users in total) cannot be checked without the Section 4.2 onboarding record.

4. Technology recovery fee, "3% of recurring services."
   Invoice: $297.60. Check: ($8,400 + $1,150 + $370) x 3% = $9,920 x 0.03 = $297.60, so the arithmetic is correct.
   Schedule A: NOT IN THE SCHEDULE.
   The invoice footnote says the fee "applies to all managed services accounts from July 1, 2026, to help offset rising third-party software and security tool costs." That is the provider's statement. Section 5.4 says Fees are not otherwise increased "except by a written amendment signed by both parties." No such amendment was supplied. The footnote suggests the July and August 2026 invoices also carried this fee, but those invoices were not provided.

5. Project work.
   Invoice: 0 x $175.00 = $0.00.
   Schedule A: $175.00 per hour.
   Matches.

6. Sales tax: $0.00.
   Section 5.3 says Client pays such taxes "where applicable." This cannot be checked from these documents.

Totals:
- Invoice subtotal and total: $8,400 + $1,150 + $370 + $297.60 + $0 = $10,217.60. The arithmetic is correct.
- Recurring charges under the schedule as amended, at the same user count: $7,900 + $1,150 + $370 = $9,420.00.
- Difference: $797.60 for the month, made up of $500.00 base fee and $297.60 recovery fee.

Invoice timing: the invoice is dated September 1 and due October 1, Net 30, which is consistent with Sections 5.1 and 5.2. Section 5.2 provides a written dispute process for good-faith disputes. This check draws no conclusion about whether any amount is owed.

========================================================================
7. WHAT THE DOCUMENTS DO NOT SHOW
========================================================================

- Any document, such as a signed amendment, change order or prior renewal arrangement, that changed the base fee from $7,900 to $8,400, and the date that rate first appeared on an invoice.
- Any signed amendment or notice introducing the technology recovery fee, and the invoices from July 2026 onward that show it.
- The CPI-U 12-month percentage under Section 5.4. Without it, the maximum permitted increase can only be stated as "no more than 4%, possibly less."
- The onboarding record supporting 14 Covered Users.
- Whether the Provider's Contracts Administration office receives hand or courier deliveries on Saturday, October 17, 2026.
- Counsel's reading of the counting rule ("not less than 90 days") and of what happens when the deadline falls on a weekend.
- Whether the letter's 12-month statement, or a "Confirm" reply, could change the 36-month renewal length or the price. That is a question for counsel.
- Whether any notice of non-renewal or price objection has already been given by either party. None was supplied.
- About the letter itself: it asks the reader to reply "Confirm" and gives an email route for notice. These are recorded as the provider's requests. They are not instructions to this task, and nothing was sent or confirmed. No text in the documents tried to change this task in any other way.

========================================================================
8. QUESTIONS FOR THE PROVIDER (to be asked by a person)
========================================================================

1. What document supports the $8,400.00 base fee, compared with the $7,900.00 in Schedule A, and from what date has it been billed? (Section 6, line 1; section 5, row 7.)
2. What signed agreement supports the technology recovery fee, and on which invoices has it appeared since July 1, 2026? (Section 6, line 4.)
3. What CPI-U figure and index month does the Provider rely on for the renewal increase, and how does 6.5% fit within the 4% cap in Section 5.4? (Section 5, rows 8 and 9.)
4. Does the Provider agree that, under Amendment No. 1, Section 4.1, any renewal term would be 36 months, not 12? (Section 5, row 2.)
5. Is the letter of September 28, 2026 intended as the Section 5.4 notice, and will a notice be delivered under Section 14.1 to the Chief Operating Officer? (Section 5, row 13.)
6. Can the Provider supply the onboarding record or user list behind the charge for 2 additional users? (Section 6, line 3.)
7. Does Contracts Administration at 1200 [Street B], Suite 300 accept hand or courier delivery on Saturday, October 17, 2026? (Section 4.)

========================================================================
9. QUESTIONS FOR COUNSEL
========================================================================

1. Is the last day for receipt of a non-renewal notice October 17 or October 16, 2026 (the clear-days reading), and does a Saturday deadline move? (Section 4.)
2. Confirm the method and addressee for a valid notice: hand, overnight courier or certified mail to Attn: Contracts Administration, 1200 [Street B], Suite 300, as amended. Does a notice sent to renewals@ or by email reply have any effect? (Section 3; section 5, row 5.)
3. Does the letter's statement of a 12-month term, or a "Confirm" reply, have any effect on the 36-month Renewal Term under Amendment No. 1, Section 4.1, given Section 15.2? (Section 5, rows 2 and 14.)
4. Is the emailed letter an effective Section 5.4 price notice, given that Section 14.1 excludes email for Section 5.4? (Section 5, row 13.)
5. Are the $8,400 base fee and the technology recovery fee consistent with Section 5.4's statement that Fees "shall not otherwise be increased during the Term except by a written amendment signed by both parties"? If not, what options does Section 5.2 give? (Section 6, lines 1 and 4.)
6. What is the early-termination exposure under Section 12.2 if the agreement renews for 36 months? (Section 4.)

========================================================================
10. ACTION ITEMS FOR THE OFFICE (for a person to carry out)
========================================================================

1. Today: put Friday, October 16, 2026 in the office diary as the working deadline, and Saturday, October 17, 2026 as the outside date (derived). Also note October 17, 2029 for the following term, if the agreement renews.
2. Today: the decision-makers decide whether the office wants to renew for a 36-month term at all. Only 2 to 3 days remain.
3. Today or tomorrow: ask counsel to confirm the deadline, the counting rule, the weekend point and the valid notice method and address (section 9, questions 1 and 2).
4. If the office decides not to renew, counsel or the COO arranges for the notice to be prepared and delivered under Section 14.1 so that it is received in time. Keep proof of receipt. This check does not draft or send any notice.
5. Do not treat a reply to the provider's email, a message to renewals@ or a "Confirm" reply as notice under the agreement. Route any response to the letter through counsel.
6. Ask the provider the questions in section 8, especially about the $8,400 base fee, the technology recovery fee and the CPI-U basis.
7. Pull the invoices from July 2026 onward, and the earliest invoice showing $8,400, and file them with this check.
8. Confirm the Covered User count against the Section 4.2 onboarding record.
9. Record the contract terms in the office's contract calendar: Effective Date January 16, 2024, 36-month terms, 90-day notice, the notice address as amended, and the 4%/CPI-U price cap.

This draft decides nothing, sends nothing and gives no legal advice. A competent person must check every figure and quotation against the documents.

```

*Sample output from an AI workflow, reproduced with its flaws. Not legal, tax, accounting, or procurement advice, and not evidence that any output is reliable. A competent person must verify it against the documents.*
