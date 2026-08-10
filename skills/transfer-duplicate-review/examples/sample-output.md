# Transfer and Duplicate Review

**Period:** May 1 to May 31
**Accounts reviewed:** Operating, Reserve (Operating LLC); Property (Property LLC)
**Prepared by:** [Preparer]
**Date:** [Date]
**Status:** Draft for review. No row has been excluded and nothing has been booked.

> Groupings below are proposed from the material provided and are unverified. Each carries the evidence that produced it, so you can disagree with a specific test rather than the conclusion. Items marked *(assumption)* are inferred; items marked *(missing)* were not provided.

---

## 1. Group summary

| Classification | Groups | Rows |
|---|---|---|
| Internal transfer | 1 | 2 |
| Inter-entity transfer | 1 | 2 |
| Pending and settled pair | 1 | 2 |
| Genuine external flow | 3 | 3 |
| Unmatched | 1 | 1 |
| **Total** | **7** | **10** |

Rows account for the 10 provided. **Duplicate representations identified: 3.**

## 2. Group detail

### G1: Internal transfer, 25,000.00

| Account | Date | Description | Amount |
|---|---|---|---|
| Operating | 05/04 | Transfer out to reserve | -25,000.00 |
| Reserve | 05/04 | Transfer in | 25,000.00 |

**One economic event:** a movement of 25,000.00 between two accounts of Operating LLC.
**Evidence:** same date, exactly opposite amounts, and both descriptions name a transfer. Both accounts belong to the same entity.
**Primary representation:** the Operating account row. The Reserve row restates the same event.

*This is one event requiring both a debit and a credit. The duplicate here is the second source row, not an accounting leg.*

### G2: Inter-entity transfer, 40,000.00 gross, with a 25.00 difference

| Account | Date | Description | Amount |
|---|---|---|---|
| Operating (Operating LLC) | 05/11 | Outgoing wire, memo "to property" | -40,000.00 |
| Property (Property LLC) | 05/12 | Deposit, memo "funding" | 39,975.00 |

**One economic event *(assumption)*:** a movement of 40,000.00 from Operating LLC to Property LLC, arriving 25.00 lighter.
**Evidence:** consecutive dates inside the settlement window, memos that correspond, and a difference consistent with an intermediary fee.
**Gross and difference reported separately:** gross 40,000.00, difference 25.00. **Not netted.**

> **This group is not a deduplication question.** It crosses two legal entities, which raises how the movement should be recorded between them. That follows the office's agreements and policy and is **not determined here.** See *Requires a person*.

### G3: Pending and settled pair, Harbor Restaurant

| Account | Date | Description | Amount | Status |
|---|---|---|---|---|
| Operating | 05/18 | Card authorization, Harbor Restaurant | -862.40 | Pending |
| Operating | 05/19 | Card purchase, HARBOR RESTAURANT | -879.65 | Settled |

**One economic event *(assumption)*:** a single card purchase, authorized 05/18 and settled 05/19 at 879.65.
**Evidence:** same account, consecutive dates, same merchant after normalizing case, and a 17.25 increase consistent with a gratuity added at settlement.
**Surviving representation:** the settled row, 879.65.
**Superseded:** the pending row, 862.40. Link retained to the settled row.

*The amount difference does not disprove the pair, and a matching amount would not have proved one.*

### G4 to G6: Genuine external flows

| Account | Date | Description | Amount |
|---|---|---|---|
| Operating | 05/07 | Payment, Landscaping Co | -3,500.00 |
| Property | 05/08 | Payment, Roofing Co | -3,500.00 |
| Property | 05/21 | Payment, Utility Co | -6,300.00 |

**Deliberately not grouped.** The 05/07 and 05/08 rows are the same amount on consecutive days across two accounts, which is the shape of an inter-entity transfer. They are **not** grouped, because both are outflows rather than opposite-signed, and they name different counterparties. Similar amount and timing is evidence, not proof.

### G7: Unmatched

| Account | Date | Description | Amount |
|---|---|---|---|
| Reserve | 05/26 | Withdrawal, memo "REF 4471" | -12,000.00 |

An outflow with no counterpart in the accounts provided. This does **not** mean no counterpart exists. See *Gaps*.

## 3. Duplicate representations

Rows that restate an event already represented elsewhere. **None has been excluded.**

| Account | Date | Amount | Restates | Basis |
|---|---|---|---|---|
| Reserve | 05/04 | 25,000.00 | G1, Operating 05/04 | Same date, opposite amount, same entity, transfer descriptions |
| Property | 05/12 | 39,975.00 | G2, Operating 05/11 | Within settlement window, corresponding memos, fee-consistent difference |
| Operating | 05/18 | 862.40 | G3, Operating 05/19 | Same account and merchant, consecutive dates, settlement-consistent increase |

## 4. Requires a person

| Item | Question to resolve |
|---|---|
| **G2, inter-entity movement** | How is a movement from Operating LLC to Property LLC recorded between the entities? The answer follows the office's agreements and policy, and the possibilities carry materially different treatment. Not determined here. |
| **G2, 25.00 difference** | Confirm the difference is an intermediary fee rather than a partial deduction or a second movement. No fee convention was provided *(missing)*. |
| **G3, gratuity inference** | Confirm the 17.25 increase is a gratuity rather than a second charge at the same merchant. |
| **G7, unmatched 12,000.00** | Identify the counterparty. "REF 4471" is not resolvable from the material provided. |
| **Classification overlap** | G2 carries both a cross-entity attribute and a fee. It is reported under the more consequential one. Confirm that reading. |

## 5. Gaps and assumptions

- **Not all accounts were provided.** The entity map names other entities whose accounts were not supplied. A counterpart sitting in one of those accounts **could not have been found**, so G7 being unmatched is a limit of the input, not a finding about the movement.
- **No amount tolerance provided** *(missing)*. The 25.00 and 17.25 differences are reported as differences rather than as acceptable variances.
- **No fee conventions documented** *(missing)*. The 25.00 is described as fee-consistent, not identified as a fee.
- **Two groups rest on memo correspondence** *(assumption)*. G2 relies on "to property" and "funding" corresponding. That is suggestive, not conclusive, and the entities differ, so the cost of being wrong is higher than usual.
- **No row was excluded.** Every duplicate identified above remains traceable to the event it restates.

---

*This review is an unverified draft for human review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It books nothing, excludes nothing, and determines no intercompany treatment. A competent person must verify every proposed grouping against source records before any row is treated as a duplicate.*
