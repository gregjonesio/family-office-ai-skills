# Sample output: Entity Compliance Calendar

The output of a fresh AI session given the current [SKILL.md](../SKILL.md) and the seven fictional documents in [sample-input.md](sample-input.md) (the same documents as the [test kit](../test-kit/)), on 2026-10-21, reproduced verbatim. This is run 1 in the [test kit results](../test-kit/README.md#results-so-far). The exact prompt is in the [test kit README](../test-kit/README.md#the-prompt-used). The session was instructed to read only those eight files; it was not technically prevented from reading others.

**Known errors and flaws in this output**, found when it was scored against the [answer key](../test-kit/answer-key.md) and when that scoring was independently reviewed, and left in place rather than edited out:

- **Error.** Section 5 says of the Manager's reappointment "It is overdue as a matter of record". The operating agreement says the Manager "may be reappointed" and sets no date for doing so, and section 1 of the same output says "None of these is concluded to have been missed".
- **Error.** Section 5 cites "appointment by Majority Interest written consent (OA 6.1, 6.2)". The excerpts cover reappointing the named Manager and removal; neither says how a replacement is appointed.
- **Error.** Section 6a says the register's December 31 year end "would move ... the quarterly counts". The quarter ends are defined separately in section 1.5.
- The dated calendar omits the [State B] notice's June 30, 2027 threshold (an unfiled registration may be revoked after notice), though section 1 lists it for earlier years.
- Section 3 calls four weekday dates "a Business Day" although the documents do not say when banks in [City C] close.
- The action items say "Enter every date in section 3 into the office calendar" before counsel and the accountant confirm them, and "Decide whether to keep [Agent A]" by July 2 without the written notice cancellation requires or the warning that cancelling does not appoint a replacement agent.
- The action items tell the office "Do not send the [State B] filing PIN by email reply", which directs the office's response rather than describing the provider's request.
- One action item sets a date of its own ("By Fri Oct 23, 2026") without saying it is a working date, not a document's.
- Action items are out of date order in one place ("By mid-August 2027" before "By Fri Jul 2, 2027").
- Section 1 lists every earlier-year obligation with no record; each is true to the documents, but the volume buries the Manager's term and the fiscal 2026 meeting.
- About 3,800 words.

It found all thirteen benchmark entries and all five restraint traps held; no date, weekday or count checked was wrong. Finding the benchmark entries does not show the calendar is complete (see the omitted date above). It is an unverified draft for human review, not legal, tax, accounting or compliance advice. Counsel and the accountant confirm the obligations and the dates before anyone relies on them.

```text
ENTITY COMPLIANCE CALENDAR (DRAFT)
[Entity A] Holdings LLC, [State A] File No. 23-4471902, [State B] ID FL-0577312
Built Wednesday, October 21, 2026, for October 21, 2026 through October 31, 2027

This is a draft built only from the seven documents provided. A person must check it against them. It is not legal, tax or compliance advice, it makes no filing, and it does not say whether the entity is in good standing.

Counting convention: for "within N days after" a period end, the day after the period end is day 1 (for example, July 1 is day 1 after June 30). "OA" means the operating agreement. OA dates move under OA 14.6: "If the last day ... falls on a day that is not a Business Day, such last day shall be extended to the next succeeding Business Day." I applied that rule only to OA dates. The documents do not list the days banks in [City C] close, so each extended date assumes the bank is open that day.

======================================================================
1. ALREADY PASSED OR DUE SOON
======================================================================

DUE WITHIN 30 DAYS

- Wed Oct 28, 2026 (7 days left): Manager delivers the FY ended June 30, 2026 financial statements to each Member. Source: OA 9.2, "Within one hundred twenty (120) days after the end of each Fiscal Year". Count: June 30 + 120 days goes Jul 31 = 31, Aug 31 = 62, Sep 30 = 92, Oct 28 = 120. Watch-out: the accountant's email of Oct 5, 2026 says these statements "are in review and we expect to deliver them to you in mid-November", which is after Oct 28. See sections 6 and 8.

- Mon Nov 16, 2026 (26 days left): Manager delivers each Member's capital account statement for the quarter ended Sep 30, 2026. Source: OA 9.1, "Within forty-five (45) days after the end of each Fiscal Quarter". Count: Sep 30 + 45 days goes Oct 31 = 31, Nov 14 = 45. Nov 14 is a Saturday, so OA 14.6 moves it to Monday Nov 16.

ALREADY PASSED, NO RECORD IN THE DOCUMENTS THAT IT WAS DONE

None of these is concluded to have been missed. Each one needs checking.

- Sun Jul 19, 2026 (94 days ago): the Manager's term ended. Source: OA 6.1, "[Manager A] is hereby appointed as the Manager for a term ending on the third anniversary of the Effective Date." The Effective Date is July 19, 2023, the filing date (OA 1.3 and the Certificate). Reappointment needs "the written consent of Members holding a Majority Interest". No consent was provided. The register (last updated Mar 3, 2025) still lists [Manager A]. July 19, 2026 was a Sunday; whether OA 14.6 applies to a term ending is not clear.

- Mon Sep 28, 2026 (23 days ago): last day for the annual meeting on the FY ended June 30, 2026. Source: OA 7.1, "within ninety (90) days after the end of each Fiscal Year". Count: Jul 31 = 31, Aug 31 = 62, Sep 28 = 90. There is no record of a meeting or of a written consent under OA 7.3.

- Sun Sep 28, 2025 (388 days ago; Mon Sep 29, 2025 if OA 14.6 applies): same requirement for the FY ended June 30, 2025. No record. The register records only "Annual meeting held September 2024", and the register was last updated before this date.

- Fri Aug 14, 2026 (68 days ago): capital account statements for the quarter ended June 30, 2026 (OA 9.1). Count: Jul 31 = 31, Aug 14 = 45. No record. The earlier quarterly statements, every quarter from the one ended Sep 30, 2023 onward, also have no record.

- Mon Mar 16, 2026 (219 days ago): tax information to Members for Taxable Year 2025. Source: OA 9.3, "Within seventy-five (75) days after the end of each Taxable Year". Count: Jan 31 = 31, Feb 28 = 59, Mar 16 = 75. No record. Earlier years: Taxable Year 2024 was due Sun Mar 16, 2025 (Mon Mar 17 under OA 14.6), and Taxable Year 2023 was due Fri Mar 15, 2024 (2024 is a leap year). No record for either.

- Tue Oct 28, 2025 (358 days ago) and Mon Oct 28, 2024 (723 days ago): annual financial statements for the FYs ended June 30, 2025 and June 30, 2024 (OA 9.2). No record.

- [State B] annual reports for 2025 (window closed Tue Apr 15, 2025, 554 days ago) and 2026 (window closed Wed Apr 15, 2026, 189 days ago). The notice says reports are due "beginning with the year after the year of registration". Registration was Feb 2, 2024, so 2025 is the first year. No record of either report. The same notice also sets a June 30 date that follows the window, and both June 30, 2025 and June 30, 2026 have passed. See section 8.

- [State A] annual reports for 2024 (due Wed Jul 31, 2024, 812 days ago) and 2025 (due Thu Jul 31, 2025, 447 days ago). No record. The only one recorded is the 2026 report, "received and filed on July 8, 2026. Status: Active." The notice does not say whether a report was due for 2023, the year of formation.

======================================================================
2. DOCUMENTS READ
======================================================================

1. Certificate of Formation, [State A]. Filed July 19, 2023 at 10:42 AM; executed July 14, 2023; effective on filing; perpetual duration; registered agent [Agent A].
2. LLC Agreement (excerpts), dated as of July 1, 2023, effective as of the Effective Date (OA 2.1).
   Not provided: OA 1.8 to 1.22, Articles 3 to 5, 6.3 to 6.9, Articles 10 to 13 (including tax matters), 14.1 to 14.5, the signature pages, Schedule A (Members and Percentage Interests), and any amendments.
3. [State A] annual report acknowledgment, July 8, 2026.
4. [State B] Certificate of Registration (issued Feb 2, 2024) and a general notice to registered foreign LLCs (undated).
5. [Agent A] renewal notice, Sep 30, 2026, and [Agent B] invoice email INV-55821, Oct 12, 2026.
   Not provided: the invoice attachment, and [Agent A]'s compliance package terms.
6. Accountant's email, Oct 5, 2026.
   Not provided: a signed engagement letter (mentioned), the June 30 trial balance, and the financial statements now in review.
7. The office's register entry, last updated Mar 3, 2025.
   Not provided: the minute book, including the September 2024 minutes.

Referred to but also not provided:
- the [State A] online filing account, which holds the annual tax amount
- any earlier [State A] or [State B] annual reports
- any written consent reappointing the Manager

======================================================================
3. THE CALENDAR (Oct 21, 2026 to Oct 31, 2027)
======================================================================

Wed Oct 28, 2026 (derived)
- What: FY2026 (FY ended June 30, 2026) financial statements to each Member.
- Who: Manager.
- Source: OA 9.2.
- Count: June 30, 2026 + 120 days = Oct 28. It is a Business Day.

Mon Nov 16, 2026 (derived)
- What: capital account statements for the quarter ended Sep 30, 2026.
- Who: Manager.
- Source: OA 9.1 and 14.6.
- Count: Sep 30 + 45 days = Sat Nov 14, moved to Mon Nov 16.

Tue Dec 15, 2026 (stated)
- What: [Agent B] invoice INV-55821 for $189.00 is due. It covers [State B] registered agent service from Jan 1 to Dec 31, 2027.
- Who: the email is addressed to the Office Manager.
- Source: Doc 5, Part 2, "Due date December 15, 2026".

Fri Jan 1, 2027 (stated)
- What: the [State B] 2027 annual report filing period opens.
- Who: not named. OA 2.2 says the Manager "shall cause all reports required ... to be filed when due".
- Source: Doc 4, Part 2, "January 1 through April 15 of each year".

Mon Feb 1, 2027 (stated)
- What: the 2026 trial balance and the Members' capital activity for 2026 go to the accountant.
- Who: the office.
- Source: Doc 6, "by February 1, 2027".

Mon Feb 15, 2027 (derived)
- What: capital account statements for the quarter ended Dec 31, 2026.
- Who: Manager.
- Source: OA 9.1 and 14.6.
- Count: Dec 31 + 45 days goes Jan 31 = 31, Feb 14 = 45. Feb 14 is a Sunday, so it moves to Mon Feb 15, if banks in [City C] are open that day.

Mon Mar 15, 2027 (stated)
- What: the 2026 partnership return is due.
- Who: the accountant.
- Source: Doc 6, "due March 15, 2027".

Tue Mar 16, 2027 (derived)
- What: tax information to each Member for Taxable Year 2026 (the calendar year, OA 1.7).
- Who: Manager.
- Source: OA 9.3.
- Count: Dec 31, 2026 + 75 days goes Jan 31 = 31, Feb 28 = 59, Mar 16 = 75. It is a Business Day.

Thu Apr 15, 2027 (stated)
- What: the [State B] 2027 annual report filing period closes. The report confirms the registered agent, principal office and managers. The fee is not stated.
- Who: not named (see OA 2.2).
- Source: Doc 4, Part 2.

Mon May 17, 2027 (derived)
- What: capital account statements for the quarter ended Mar 31, 2027.
- Who: Manager.
- Source: OA 9.1 and 14.6.
- Count: Mar 31 + 45 days goes Apr 30 = 30, May 15 = 45. May 15 is a Saturday, so it moves to Mon May 17.

Wed Jun 30, 2027 (stated, reference date)
- What: Fiscal Year 2027 and its fourth Fiscal Quarter end. This date starts the counts for the July to October 2027 entries.
- Source: OA 1.4 and 1.5.

Thu Jul 1 to Tue Sep 28, 2027 (derived)
- What: the window for the annual meeting on FY2027. Notice rules are in section 5.
- Who: Manager sets the time and place.
- Source: OA 7.1.
- Count: June 30 + 90 days goes Jul 31 = 31, Aug 31 = 62, Sep 28 = 90.

Fri Jul 2, 2027 (derived)
- What: the last day to give [Agent A] written notice of cancellation, only if the office decides not to renew. "No action is needed to continue service."
- Who: the office decides.
- Source: Doc 5, Part 1, "at least 30 days before the renewal date".
- Count: Aug 1 minus 30 days = Jul 2. Not moved; this is a provider date.

Sat Jul 31, 2027 (derived)
- What: the [State A] 2027 annual report is due, with the annual tax "payable with the report". The amount is not given. Filing is online only, and the state sends no paper reminders. [Agent A] does not file the report.
- Who: not named (see OA 2.2).
- Source: Doc 3, "due on or before the last day of the month in which the company was formed". The company was formed (filed) on July 19, 2023, so the month is July.
- Weekend: July 31 is a SATURDAY. No [State A] document gives a weekend rule, so the date is NOT moved.

Sun Aug 1, 2027 (stated)
- What: [Agent A] service renews automatically "at the then-current annual fee, currently $299.00".
- Who: [Agent A].
- Source: Doc 5, Part 1.
- Weekend: Aug 1 is a SUNDAY. Not moved.

Mon Aug 16, 2027 (derived)
- What: capital account statements for the quarter ended June 30, 2027.
- Who: Manager.
- Source: OA 9.1 and 14.6.
- Count: Jun 30 + 45 days goes Jul 31 = 31, Aug 14 = 45. Aug 14 is a Saturday, so it moves to Mon Aug 16.

Wed Sep 15, 2027 (stated, conditional)
- What: the extended due date for the 2026 partnership return, only if an extension is filed.
- Who: the accountant.
- Source: Doc 6, "we'll file an extension, which takes the return to September 15, 2027".

Tue Sep 28, 2027 (derived)
- What: the last day of the FY2027 annual meeting window.
- Who: Manager.
- Source: OA 7.1.
- It is a Business Day.

Thu Oct 28, 2027 (derived)
- What: FY2027 financial statements to each Member.
- Who: Manager.
- Source: OA 9.2.
- Count: June 30, 2027 + 120 days goes Jul 31 = 31, Aug 31 = 62, Sep 30 = 92, Oct 28 = 120. It is a Business Day.

Just after the period: capital statements for the quarter ended Sep 30, 2027 fall due Sun Nov 14, 2027, which moves to Mon Nov 15, 2027.

======================================================================
4. THE RULES BEHIND THE DATES
======================================================================

Each rule is quoted so the calendar can be extended past the period.

- [State A] annual report and tax (Doc 3): "The annual report is due on or before the last day of the month in which the company was formed (its anniversary month)." This gives July 31 every year. "The annual tax amount ... is payable with the report."
- [State B] annual report (Doc 4): "during the filing period of January 1 through April 15 of each year, beginning with the year after the year of registration." "A report filed after April 15 is subject to a late fee. A registration for which no report has been filed by the following June 30 may be revoked after notice." Neither fee is stated.
- Annual meeting (OA 7.1): "within ninety (90) days after the end of each Fiscal Year". The Fiscal Year ends June 30 (OA 1.4), so the last day is Sep 28 each year.
- Meeting notice (OA 7.2): "not less than ten (10) nor more than sixty (60) days before the meeting."
- Quarterly capital statements (OA 9.1): 45 days after Sep 30, Dec 31, Mar 31 and Jun 30 (OA 1.5).
- Annual financial statements (OA 9.2): 120 days after June 30, which is Oct 28.
- Member tax information (OA 9.3): 75 days after Dec 31 (Taxable Year = calendar year, OA 1.7). That is Mar 16 in a common year and Mar 15 in a leap year.
- Manager term (OA 6.1): ends on the third anniversary of the Effective Date (July 19, 2023, per OA 1.3, not the "dated as of" date of July 1, 2023). The Manager "may be reappointed for a further term of three years" by Majority Interest written consent.
- Business Day extension (OA 14.6, OA dates only), using the Business Day definition in OA 1.1.
- [Agent A] (Doc 5, Part 1): renews each August 1 for one year; written cancellation at least 30 days before.
- [Agent B] (Doc 5, Part 2): service runs by calendar year, invoiced in advance.
- Accountant (Doc 6, 2026 tax year only):
  - data due Feb 1
  - return due Mar 15, or Sep 15 if extended
  - "Members' tax packages go out once the return is final."
  The email does not state these as a recurring rule.

======================================================================
5. OBLIGATIONS WITHOUT A DATE
======================================================================

- FY2027 annual meeting: the date is to be set by the Manager within Jul 1 to Sep 28, 2027. Notice goes out 10 to 60 days before (OA 7.2).
  - If the meeting is held on Sep 28, 2027, the notice window would run from Fri Jul 30 to Sat Sep 18, 2027.
  - It is unclear whether the "10 days" count includes the meeting day.
  - It is also unclear whether OA 14.6 could push a Saturday notice deadline to Monday when that would cut the minimum notice period.
  - Under OA 7.3, written consent may replace a meeting for "any action that may be taken at a meeting".
- Manager reappointment or appointment by Majority Interest written consent (OA 6.1, 6.2). It is overdue as a matter of record (section 1). No date is set.
- Minutes of every meeting and every written consent must be kept with the books (OA 8.1). This arises with each meeting or consent.
- Extension of the 2026 partnership return: "If anything comes in late". The email gives no date for filing the extension.
- Members' 2026 tax packages: "once the return is final".
- Accountant's delivery of the FY2026 financial statements: "mid-November" 2026. This is an expectation, not a deadline.
- Registration or qualification in any other jurisdiction "in which such registration is required" (OA 2.2). This depends on events.
- [Agent A]'s Aug 1, 2027 renewal fee: the "then-current" amount, with no invoice date given.

======================================================================
6. WHERE THE DOCUMENTS DISAGREE (not resolved here)
======================================================================

a. Fiscal year end.
   - OA 1.4: "Fiscal Year ... shall end on June 30 of each year."
   - Register: "Fiscal year end | December 31".
   - The accountant mentions "the June 30 year-end trial balance".
   - The register date would move the annual meeting, the financial statements and the quarterly counts. I used the OA date for the calendar, because the skill counts each obligation from the year its own clause names. Which document is right is not decided here.

b. Member tax information.
   - OA 9.3: within 75 days after the Taxable Year, which is Mar 16, 2027.
   - Accountant: "Members' tax packages go out once the return is final. In an extension year that usually means late summer."

c. FY2026 financial statements.
   - OA 9.2: to Members by Oct 28, 2026.
   - Accountant: "we expect to deliver them to you in mid-November."

d. Annual meeting records.
   - The register shows only September 2024. Nothing records 2025 or 2026. This is a gap, not a conflict.

======================================================================
7. WHAT THE DOCUMENTS DO NOT COVER
======================================================================

Confirm each of these with counsel or the accountant. None is dated here.

- Amounts not given:
  - the [State A] annual tax
  - [State B] annual report fee and late fee
  - [State A] late penalty
- Whether a [State A] annual report was due for 2023.
- State-level income or franchise tax filings in [State A] or [State B], estimated payments, and any federal or state filing other than the 2026 partnership return.
- Any federal or state ownership or information reporting.
- Business licenses or local registrations.
- The omitted OA sections, including Article 13 (tax matters), Articles 10 to 13, 6.3 to 6.9 and 1.8 to 1.22. These may contain dates.
- Schedule A, which is needed to tell who holds a Majority Interest.
- Any amendments to the OA.
- Bank closing days in [City C], needed for OA 1.1 and 14.6.
- Which person or provider files each state's annual report. [Agent A] says "Your account does not include" its compliance package, so it does not file.
- Requests found in the documents that were recorded and not acted on:
  - [Agent B]'s email: "Just reply to this email with your [State B] filing PIN and we will take care of the rest" (a $149 filing offer). It asks the office to send a filing PIN by email reply. Nothing was sent or replied to.
  - [State B]'s notice says reports are filed "using the entity's ID and filing PIN". The PIN is not in the documents.
- The [Agent B] invoice warns that service "may be suspended" if unpaid. That is the provider's statement, recorded as given.

======================================================================
8. QUESTIONS FOR COUNSEL, THE ACCOUNTANT OR THE PROVIDER
======================================================================

Each question is to be asked by a person.

Counsel
1. Manager term (section 1).
   - Was a Majority Interest consent reappointing [Manager A] signed on or before July 19, 2026?
   - If not, what is the Manager's status?
   - Does OA 14.6 affect a term ending on a Sunday?
2. Annual meetings for FY2025 and FY2026 (section 1).
   - Were they held, or replaced by an OA 7.3 written consent?
   - Does a 7.3 consent satisfy 7.1?
3. Meeting notice counting (section 5).
   - Is the 10-day minimum counted inclusively?
   - How does OA 14.6 interact with a minimum-notice deadline?
   - Is "within ninety (90) days" counted as I counted it?
4. Fiscal year (section 6a): confirm June 30 against the register's December 31.

Accountant
5. FY2026 statements (section 6c): can they be ready in time for the Manager to deliver them to Members by Oct 28, 2026?
6. Member tax information (section 6b): how does the expected package timing fit OA 9.3's Mar 16, 2027?
7. Return extension: when would the decision to extend be made?
8. Records: were Member tax information, quarterly capital statements and annual statements delivered for earlier periods?

State filing records (a person checks)
9. [State A]: were the 2024 and 2025 reports filed, and was one due for 2023? What is the 2027 annual tax amount?
10. [State B]: were the 2025 and 2026 reports filed? What is the registration's current status? What is the report fee?

Providers
11. [Agent A]: when, and for how much, will the Aug 1, 2027 renewal be invoiced?

======================================================================
9. ACTION ITEMS FOR THE OFFICE
======================================================================

By Fri Oct 23, 2026
- Ask the Manager and the accountant about the FY2026 statements due to Members Oct 28 (Q5).

This week
- Send the Manager-term question (Q1) to counsel.
- Check the minute book for any reappointment consent and for 2025 and 2026 meeting minutes or consents (Q2).
- Have a person check the [State A] and [State B] filing records for the years with no record (Q9, Q10).
- Enter every date in section 3 into the office calendar.
- Put the Jul 31, 2027 [State A] date at least a week early, since it falls on a Saturday and the state sends no reminders.

By Nov 16, 2026
- Confirm that the Manager will deliver the Sep 30, 2026 quarter capital statements.

By Dec 15, 2026
- A person decides on, and processes through the office's normal approval, [Agent B] invoice INV-55821 ($189.00).
- Do not send the [State B] filing PIN by email reply.
- Decide separately whether to engage anyone to file the [State B] report.

Early January 2027
- Decide who files the [State B] 2027 report (window Jan 1 to Apr 15).
- Start assembling the 2026 trial balance and capital activity, due to the accountant Feb 1.

After counsel confirms
- Update the register: fiscal year end, Manager status, annual meeting history, and the "last updated" date.

By mid-August 2027
- Ask the Manager to set the FY2027 annual meeting date within Jul 1 to Sep 28 and send notice 10 to 60 days ahead.

By Fri Jul 2, 2027
- Decide whether to keep [Agent A]. No action is needed to renew.

By early July 2027
- Assign who files the [State A] 2027 report and pays the tax, due Sat Jul 31, 2027.

Ongoing
- File every meeting minute and written consent in the minute book (OA 8.1).
- Confirm that each OA date falls on a [City C] bank Business Day.

Nothing in this draft was filed, paid, replied to, or entered into any system. Every date and count above should be checked against the source documents before use.
```

---

*Sample output of an AI workflow on fictional documents, reproduced with its known errors and flaws. Not legal, tax, accounting or compliance advice. It makes no filing. A competent person must verify any calendar against the documents, and counsel and the accountant confirm the obligations and the dates.*
