# Sample output: Insurance Renewal Comparison

The output of a fresh AI session given [SKILL.md](../SKILL.md) and the three fictional documents in [sample-input.md](sample-input.md) (the same documents as the [test kit](../test-kit/)), on 2026-09-30, reproduced verbatim. The exact prompt is in the [test kit README](../test-kit/README.md#the-prompt-used). The session was instructed to read only those four files; it was not technically prevented from reading others.

**Known flaws in this output**, found when it was scored against the [answer key](../test-kit/answer-key.md), and left in place rather than edited out:

- C13 and C16 label the removed wristwatch and the new theft condition as "not in the documents provided" for one year. Both documents were provided: the watch was removed and the condition was added, as each row's direction line correctly says. The skill's instruction on that label was clarified after this run.
- L11 names nine of the sixteen changes the letter does not mention; the full count is correct in section 2.

It found all nine benchmark changes, and no figure checked was wrong. It is an unverified draft for human review, not insurance, legal, or tax advice.

```text
RENEWAL COMPARISON: [Family] Residence Trust, private client homeowners policy
Expiring policy PCH-4418-2207-03 (Nov 1, 2025 to Nov 1, 2026) compared with renewal PCH-4418-2207-04 (Nov 1, 2026 to Nov 1, 2027)
This is a draft for the broker call. A person must check it against the documents. It is not insurance, legal or tax advice.

======================================================================
1. DOCUMENTS COMPARED
======================================================================
Provided:
- Last year's declarations page, PCH-4418-2207-03. It covers Section I and II limits, deductibles, additional coverages and endorsements, the jewelry schedule, conditions, the forms list and premium by section.
- This year's renewal declarations page, PCH-4418-2207-04, with the same sections.
- The broker's cover letter from [Broker], dated October 2, 2026, signed by [Account Executive].

Not provided:
- The policy forms for either year (PCH-100, PC-210 through PC-290, SP-300). Only form numbers and edition dates are available, so no policy wording can be compared.
- A rating worksheet, or any premium breakdown below the section level.
- A loss history or claims report.
- Any record of instructions the office gave the broker for this renewal.

Notes:
- The letter is dated October 2, 2026, which is two days after today (September 30, 2026). The office should confirm it is the final version.
- Each document carries a label calling it a fictional test document. As you instructed, they are treated as real. Nothing in the documents tried to direct or change this task.

======================================================================
2. CHANGE TABLE
======================================================================
Terms are quoted as printed. "Letter" means whether the broker's letter mentions the change.
In total there are 21 changes. The letter mentions 4, partly mentions 1 and does not mention 16.

POLICY
C1  Policy number
    Last year: "PCH-4418-2207-03"   This year: "PCH-4418-2207-04"
    Direction: the suffix moved from -03 to -04.
    Letter: partly mentioned. It cites "PCH-4418-2207" without the suffix.

C2  Policy period
    Last year: "November 1, 2025 to November 1, 2026"
    This year: "November 1, 2026 to November 1, 2027"
    Direction: moved forward one year.
    Letter: mentioned.

SECTION I: PROPERTY COVERAGES
C3  A Dwelling
    Last year: "$6,200,000"   This year: "$6,510,000"
    Direction: rose $310,000 (5.0%).
    Letter: mentioned.

C4  Extended replacement cost
    Last year: "150% of Coverage A"   This year: "125% of Coverage A"
    Direction: the percentage fell from 150% to 125%. The dollar effect is in D1.
    Letter: not mentioned.

C5  B Other structures
    Last year: "$620,000"   This year: "$651,000"
    Direction: rose $31,000 (5.0%).
    Letter: not mentioned.

C6  C Contents
    Last year: "$3,100,000"   This year: "$3,255,000"
    Direction: rose $155,000 (5.0%).
    Letter: not mentioned.

C7  D Loss of use
    Last year: "Actual loss sustained (no time limit)"
    This year: "Actual loss sustained up to 24 months"
    Direction: last year stated no time limit. This year has a 24-month limit.
    Letter: not mentioned.

DEDUCTIBLES
C8  All other perils
    Last year: "$10,000"   This year: "$25,000"
    Direction: rose $15,000 (150%).
    Letter: mentioned.

C9  Windstorm or hail, including named storm
    Last year: "$10,000"   This year: "2% of Coverage A ($130,200)"
    Direction: changed from a flat dollar amount to a percentage of Coverage A. The printed dollar figure rose $120,200 (see D4).
    Letter: not mentioned.

ADDITIONAL COVERAGES AND ENDORSEMENTS
C10 PC-210 Water backup and sump overflow
    Last year: "Included to full Coverage A limit"   This year: "$50,000"
    Direction: changed from the full Coverage A limit to a stated $50,000 (see D3). The form edition is unchanged at 04/23.
    Letter: not mentioned.

C11 PC-215 Ordinance or law
    Last year: "100% of Coverage A"   This year: "25% of Coverage A"
    Direction: the percentage fell from 100% to 25% (see D2). The form edition is unchanged at 04/23.
    Letter: not mentioned.

SCHEDULED PERSONAL PROPERTY: JEWELRY
C12 Valuation basis
    Last year: "AGREED VALUE"   This year: "STATED VALUE"
    Direction: the basis changed. The SP-300 form edition is unchanged at 04/23.
    Letter: not mentioned. The letter says only that jewelry coverage continues.

C13 Gentleman's wristwatch
    Last year: "Item 4  Gentleman's wristwatch, perpetual calendar  $38,000"
    This year: not on the renewal schedule (not in the documents provided).
    Direction: removed from the schedule. The item count fell from 6 to 5.
    Letter: not mentioned.

C14 Item numbering
    Last year: "Item 5  Pearl strand with diamond clasp  $74,000" and "Item 6  Emerald cocktail ring  $72,000"
    This year: "Item 4  Pearl strand with diamond clasp  $74,000" and "Item 5  Emerald cocktail ring  $72,000"
    Direction: renumbered. Descriptions and values are unchanged. "Item 4" now refers to a different piece.
    Letter: not mentioned.

C15 Schedule total
    Last year: "$480,000"   This year: "$442,000"
    Direction: fell $38,000 (7.9%).
    Letter: not mentioned.

CONDITIONS AND FORMS
C16 Protective device condition, PC-290
    Last year: not in the documents provided. Conditions read only "Standard policy conditions apply per form PCH-100." PC-290 is not on the forms list.
    This year: "Protective device condition (PC-290): coverage for theft applies only if the central station burglar alarm is in working order and set whenever the residence premises is unoccupied." The forms list adds "PC-290 (ed. 04/25) Protective Device Condition".
    Direction: condition added. The forms list grew from 9 forms to 10.
    Letter: not mentioned.

C17 Base policy form
    Last year: "PCH-100 (ed. 04/23)"   This year: "PCH-100 (ed. 04/25)"
    Direction: the edition date changed. The wording may have changed, and the declarations cannot show how.
    Letter: not mentioned.

PREMIUM
C18 Section I
    Last year: "$31,850"   This year: "$36,050"
    Direction: rose $4,200 (13.2%).
    Letter: not mentioned. The letter gives only the total.

C19 Section II
    Last year: "$2,140"   This year: "$2,210"
    Direction: rose $70 (3.3%). The Section II limits (E and F) are unchanged on the declarations.
    Letter: not mentioned.

C20 Scheduled personal property
    Last year: "$7,210"   This year: "$6,640"
    Direction: fell $570 (7.9%).
    Letter: not mentioned.

C21 Total annual premium
    Last year: "$41,200"   This year: "$44,900"
    Direction: rose $3,700 (9.0%).
    Letter: mentioned.

UNCHANGED ON BOTH PAGES (checked line by line)
- Transaction type ("Renewal").
- Named insured and trustees.
- Residence premises: masonry veneer, built 2009, protection class 3, 0.8 miles to coast, central station alarm "yes (fire and burglar)".
- Producer.
- E Personal liability, each occurrence: $1,000,000.
- F Medical payments, each person: $25,000.
- Earthquake: "Not covered".
- PC-230: $50,000. PC-240: "Included". PC-250: "5% annual". PC-260: "Additional 5% of Coverage A". PC-270: $50,000.
- Jewelry Items 1 to 3: ring $142,000, necklace $96,000, earrings $58,000.
- Jewelry "Deductible: none."
- The conditions line "Standard policy conditions apply per form PCH-100."
- Edition dates for PC-210 and PC-215 (04/23), PC-230 through PC-270 (01/22) and SP-300 (04/23).

======================================================================
3. LETTER CHECK
======================================================================
L1  "Enclosed is the renewal for the homeowners policy, effective November 1, 2026."
    MATCHES (C2).

L2  "Re: ... policy PCH-4418-2207"
    MATCHES the base number. The renewal carries the suffix -04 (C1).

L3  "The renewal premium is $44,900, an increase of about 9% over the expiring $41,200."
    MATCHES: +$3,700, or 8.98% (C21).
    TRUE BUT INCOMPLETE: the sections moved differently. Section I rose 13.2%, Section II rose 3.3% and scheduled property fell 7.9% (C18 to C20).

L4  "The increase reflects higher reconstruction costs and rate filings by [Carrier] for coastal homes this year."
    CANNOT BE CHECKED from these documents.
    The premises details, including distance to coast (0.8 miles), are unchanged on the declarations. Several terms changed in the same renewal (C4, C7, C8, C9, C10, C11, C12, C13, C16). The documents do not show how any of these affected the premium.

L5  "Your dwelling limit has increased 5% to $6,510,000"
    MATCHES (C3).

L6  "under the policy's inflation guard"
    CANNOT BE CHECKED. It is consistent with PC-250 "5% annual", which appears in both years, but the declarations do not say where the increase came from.

L7  "which keeps the limit in step with building costs"
    CANNOT BE CHECKED. The PC-250 wording was not provided.

    The dwelling paragraph (L5 to L7) as a whole is TRUE BUT INCOMPLETE. It leaves out four things:
    - Extended replacement cost fell from 150% to 125% of Coverage A (C4). By the derived figures in D1, the total fell from $9,300,000 to $8,137,500.
    - Coverages B and C also rose 5% (C5, C6).
    - Ordinance or law fell from 100% to 25% of Coverage A (C11).
    - Water backup changed from the full Coverage A limit to $50,000 (C10).

L8  "To help offset the increase, we have moved the all other perils deductible from $10,000 to $25,000."
    The deductible figures MATCH (C8).
    "To help offset the increase" CANNOT BE CHECKED. The documents show no premium for the $10,000 option.
    TRUE BUT INCOMPLETE: the windstorm or hail deductible also changed, from "$10,000" to "2% of Coverage A ($130,200)" (C9), and the letter does not mention it.
    Nothing in the documents shows whether the office asked for or approved the change.

L9  "We believe this is a sensible trade given the family's claims history, which remains clean."
    This is the broker's opinion. The claims history CANNOT BE CHECKED from these documents.

L10 "Your liability coverage, identity fraud, domestic staff and jewelry coverage continue on renewal."
    - Liability: MATCHES as to limits (E $1,000,000 and F $25,000 are unchanged). The base form edition changed (C17), so the wording cannot be confirmed.
    - Identity fraud: MATCHES (PC-230, $50,000, edition 01/22 in both years).
    - Domestic staff: MATCHES (PC-240, "Included", edition 01/22 in both years).
    - Jewelry: TRUE BUT INCOMPLETE. The schedule continues, but:
      - the valuation basis changed from AGREED VALUE to STATED VALUE (C12);
      - the wristwatch ($38,000) is no longer scheduled (C13);
      - the items were renumbered (C14);
      - the total fell from $480,000 to $442,000 (C15);
      - a new theft condition, PC-290, was added (C16). The documents do not show whether it applies to the jewelry.

L11 Overall: the letter mentions 4 of the 21 changes. It does not mention C4, C7, C9, C10, C11, C12, C13, C16 or C17.

======================================================================
4. DERIVED FIGURES (none of these is stated on the pages)
======================================================================
D1  Extended replacement cost in dollars (derived)
    Last year: 150% x $6,200,000 = $9,300,000
    This year: 125% x $6,510,000 = $8,137,500
    Change: $8,137,500 - $9,300,000 = -$1,162,500 (-12.5%)
    Amount above Coverage A:
    - Last year: $9,300,000 - $6,200,000 = $3,100,000
    - This year: $8,137,500 - $6,510,000 = $1,627,500
    - Change: -$1,472,500 (-47.5%)
    Assumption: "X% of Coverage A" means the total dwelling amount available, including Coverage A. If it means an amount on top of Coverage A, the "amount above Coverage A" lines do not apply (see G4).

D2  Ordinance or law in dollars (derived)
    Last year: 100% x $6,200,000 = $6,200,000
    This year: 25% x $6,510,000 = $1,627,500
    Change: -$4,572,500 (-73.75%)

D3  Water backup (derived)
    Last year: "full Coverage A limit" = $6,200,000
    This year: $50,000 (stated)
    Change: -$6,150,000
    The $50,000 is 0.77% of this year's Coverage A ($50,000 / $6,510,000).

D4  Windstorm or hail deductible
    Check of the printed figure: 2% x $6,510,000 = $130,200, which matches the declarations.
    Change: $130,200 - $10,000 = +$120,200. $130,200 / $10,000 = 13.02 times last year's figure.
    Last year's $10,000 was 0.16% of that year's Coverage A ($10,000 / $6,200,000).
    Next term (derived): $6,510,000 x 1.05 = $6,835,500, and 2% of that = $136,710. This assumes PC-250 raises Coverage A by 5% at the next renewal and the 2% term does not change.

D5  Debris removal, "Additional 5% of Coverage A" (derived)
    5% x $6,200,000 = $310,000 last year
    5% x $6,510,000 = $325,500 this year (+$15,500)
    The term is unchanged. The dollar amount moves with Coverage A.

D6  Coverages A, B and C (derived)
    - A: $6,510,000 / $6,200,000 = 1.05
    - B: $651,000 / $620,000 = 1.05
    - C: $3,255,000 / $3,100,000 = 1.05
    In both years B is 10% of A and C is 50% of A. The declarations do not say that B or C is set as a percentage of A.

D7  Premium by section (derived)
    - Section I: $36,050 - $31,850 = +$4,200, and $4,200 / $31,850 = +13.2%
    - Section II: $2,210 - $2,140 = +$70, and $70 / $2,140 = +3.3%
    - Scheduled property: $6,640 - $7,210 = -$570, and -$570 / $7,210 = -7.9%
    - Total: $44,900 - $41,200 = +$3,700, and $3,700 / $41,200 = +8.98%
    Reconciliation: $4,200 + $70 - $570 = $3,700.
    The sections add up to the stated totals in both years:
    - Last year: $31,850 + $2,140 + $7,210 = $41,200
    - This year: $36,050 + $2,210 + $6,640 = $44,900
    The Section I increase ($4,200) is larger than the total increase ($3,700).

D8  Scheduled property premium per $100 of scheduled value (derived)
    Last year: $7,210 / $480,000 x 100 = $1.502
    This year: $6,640 / $442,000 x 100 = $1.502
    The declarations do not say how this premium is calculated. This is a ratio only, not an explanation of why the premium changed.

D9  Jewelry schedule recount (derived)
    Last year, 6 items: $142,000 + $96,000 + $58,000 + $38,000 + $74,000 + $72,000 = $480,000, which matches the stated total.
    This year, 5 items: $142,000 + $96,000 + $58,000 + $74,000 + $72,000 = $442,000, which matches the stated total.
    The $38,000 difference equals the wristwatch's scheduled value.

======================================================================
5. WHAT THE DOCUMENTS DO NOT SHOW
======================================================================
G1  No policy forms for either year. PCH-100 moved from edition 04/23 to 04/25. The base policy's definitions, exclusions, conditions and settlement terms may have changed, and the declarations cannot show how. The letter's statements that coverage "continue[s]" cannot be checked against the wording.

G2  The PC-290 wording was not provided.
    - "Unoccupied", "in working order" and "set" are not defined.
    - It is not shown whether "coverage for theft" includes the scheduled jewelry under SP-300, theft away from the residence premises, or theft while domestic staff are present.
    - It is not shown what proof the carrier would need that the alarm was set.

G3  "AGREED VALUE" and "STATED VALUE" are not defined in the documents, and the SP-300 wording (edition 04/23 in both years) was not provided. How a loss to a scheduled item would be settled under either basis cannot be shown. The basis changed on the declarations while the form edition did not.

G4  Extended replacement cost. It is not shown whether "150% / 125% of Coverage A" is the total available or an amount on top of Coverage A, or what conditions apply to it. D1 depends on the answer.

G5  Loss of use, "up to 24 months". It is not shown when the 24 months starts or what it covers.

G6  Deductibles.
    - Wind: for "2% of Coverage A ($130,200)", it is not shown whether Coverage A is measured at the start of the term or at the date of loss.
    - It is not shown whether the wind deductible applies per occurrence, per named storm or per policy period, or which Section I coverages it applies to.
    - "Named storm" is not defined.
    - It is not shown whether the all other perils deductible applies per occurrence.
    - The jewelry schedule explicitly says "Deductible: none." in both years, so that point is answered.

G7  It is not stated whether these limits are per occurrence or aggregate, or whether they sit inside Coverage A or on top of it: the PC-210 $50,000, PC-215 25%, PC-230 $50,000, PC-270 $50,000 and PC-260 "Additional 5%" (the word "Additional" is printed only on PC-260).

G8  PC-250 "5% annual". It is not shown whether it applies only at renewal or also during the term, or whether it applies to Coverages B and C. B and C each rose exactly 5%, but no reason is stated.

G9  Premium. The pages show premium by section only. There is no premium by coverage or deductible, no rating detail, and no figure for the renewal on last year's terms.

G10 The letter's explanations (reconstruction costs, carrier rate filings, a clean claims history, and the deductible change as an offset) do not appear in the declarations.

G11 Authorization. Nothing shows whether the office asked for or approved any of the changes: the all other perils deductible, the wind deductible, water backup, ordinance or law, extended replacement cost, loss of use, the valuation basis, or removing the wristwatch.

G12 The documents do not say why the wristwatch was removed or whether it is insured elsewhere.

======================================================================
6. QUESTIONS FOR THE BROKER
======================================================================
THE LETTER AND CHANGES OVERALL
Q1  (L11; C4, C7, C9, C10, C11, C12, C13, C16, C17) Please give us, in writing, a complete list of every change between the expiring policy and the renewal, including wording changes in the forms.

Q2  (G11) For each change, was it required by the carrier or proposed by you? Were any of them made on an instruction from the office? If so, when was it given and by whom?

PREMIUM
Q3  (C18 to C21; L4; G9) Please provide the rating detail behind each section's change: Section I +$4,200, Section II +$70, scheduled property -$570. What documentation supports the reconstruction cost and rate filing explanation?

Q4  (C8; L8) What would the premium be with the all other perils deductible at $10,000, and is that option available?

Q5  (C4, C7, C9, C10, C11, C12, C16; G9) For each of these items, what would the premium be on last year's terms, and can each item be priced separately?

Q6  (L9) Can you provide the carrier's loss history report behind the statement that the claims history "remains clean"?

PROPERTY COVERAGES
Q7  (C4; D1; G4) Why did extended replacement cost change from 150% to 125% of Coverage A? Is the percentage the total available for the dwelling or an amount on top of Coverage A, and what conditions apply?

Q8  (C7; G5) Why was a 24-month limit added to loss of use, and when does the 24 months start?

Q9  (C11; D2; G7) Why did ordinance or law change from 100% to 25% of Coverage A? Is it inside Coverage A or on top of it? Is it per occurrence or aggregate?

Q10 (C10; D3; G7) Why did water backup change from the full Coverage A limit to $50,000? Is the $50,000 per occurrence or an annual aggregate? PC-210 kept the 04/23 edition: did only the declarations limit change?

Q11 (C3, C5, C6; D6; G8) Are the 5% increases to B and C also from PC-250? Does PC-250 adjust limits only at renewal, or also during the term?

DEDUCTIBLES
Q12 (C9; D4; G6) Why did the windstorm or hail deductible change from $10,000 to 2% of Coverage A?
    - Is Coverage A measured at the start of the term or at the date of loss?
    - Does the deductible apply per occurrence, per named storm or per policy period, and to which Section I coverages?
    - How is "named storm" defined?
    - Is a flat-dollar option available, and at what premium?
    - Does the all other perils deductible apply per occurrence?

JEWELRY
Q13 (C12; G3; D8) Why did the valuation basis change from AGREED VALUE to STATED VALUE? How would a total loss of a scheduled item be settled under each basis, and where is that defined, given SP-300 kept the 04/23 edition? Did the change affect the scheduled property rate?

Q14 (C13, C15; G12) Why was the Gentleman's wristwatch, perpetual calendar ($38,000) removed from the schedule? What instruction, if any, did you receive to remove it?

Q15 (C14) Please confirm that renumbering the pearl strand and the emerald cocktail ring is the only change to those two entries.

CONDITIONS AND FORMS
Q16 (C16; G2) Please send PC-290 (edition 04/25).
    - Why was it added?
    - Does it apply to scheduled jewelry under SP-300, and to theft away from the residence premises?
    - How are "unoccupied", "in working order" and "set" defined?
    - Is the residence "unoccupied" when domestic staff are there but the family is away?
    - What records would the carrier expect as proof that the alarm was set?

Q17 (C17; G1; L10) Please send PCH-100 in both the 04/23 and 04/25 editions, with a list of every wording change between them (a redline if one exists). Does any change affect the liability coverage the letter says continues?

======================================================================
7. ACTION ITEMS FOR THE OFFICE
======================================================================
A1  Before the call, have a person check this comparison line by line against the original declarations pages, including every derived figure.

A2  Have a person request in writing from the broker:
    - PCH-100 (both editions), PC-290, SP-300, PC-210, PC-215 and PC-250;
    - rating detail by section;
    - the complete list of changes (Q1);
    - the loss history report;
    - confirmation that the letter dated October 2, 2026 is the final version.

A3  Search the office's own records (email and meeting notes) for any instruction to the broker about the deductibles, the jewelry valuation basis or removing the wristwatch. Note what you find before the call.

A4  Confirm with whoever manages the family's jewelry what happened to the Gentleman's wristwatch, perpetual calendar (still owned, sold, gifted or moved), and whether it is insured anywhere else.

A5  Confirm with whoever manages the residence:
    - that the central station burglar alarm is monitored and working;
    - how and by whom it is set when the residence is unoccupied, including when staff are on site but the family is away;
    - whether the monitoring company keeps arming records.
    Share the PC-290 wording with them once it arrives.

A6  Update any internal jewelry records that use schedule item numbers. Item 4 is now the pearl strand, Item 5 is the emerald cocktail ring, and there is no Item 6.

A7  Share this comparison and the questions with the trustees ([Trustee A] and [Trustee B]) or whoever decides on the renewal. Schedule the broker call well before the November 1, 2026 effective date.

A8  After the call, record the broker's answers against each question number, and file this comparison with the policy record for PCH-4418-2207-04.

----------------------------------------------------------------------
This comparison makes the renewal easier to read before the broker call. It is not insurance, legal or tax advice. It does not judge whether coverage is adequate, and it does not recommend accepting, declining or changing the renewal. A competent person must check it against the documents. Have the broker, and counsel where needed, review the coverage questions before anyone acts. Using it creates no professional or fiduciary relationship.
```

*Sample output is an unverified AI draft on fictional documents, shown to model the skill's conservative behavior. It is not insurance, legal, or tax advice. A competent person must verify any comparison against the source documents.*
