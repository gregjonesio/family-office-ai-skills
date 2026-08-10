# Reconciliation Evidence Pack

**Entity:** Operating LLC
**Account:** Operating account
**Period:** June 1 to June 30
**Prepared by:** [Preparer]
**Date:** [Date]
**Status:** Evidence for review. **This pack does not reconcile the account and reaches no conclusion.**

> **The net difference on this account is 0.00. That is not a result.** Three separate items failed the tests below, and they happen to offset exactly. A reconciliation reporting only the net figure would pass this account while three genuine errors sat inside it. Read sections 2, 3, and 5 before section 4's arithmetic.

---

## 1. Evidence inventory

| Evidence | Origin | As-of | Independent of the ledger? |
|---|---|---|---|
| Ledger balance and activity | Accounting platform | June 30 | No, this is the population being tested |
| Institution statement | The institution directly | June 30 | **Yes** |
| Prior reconciling items | Prior period working papers | Feb 14 onward | Partially, derived from prior reconciliations |
| Outstanding items | Reported by the operator | June 30 | No, operator representation *(assumption)* |

As-of dates align with the period end. Both assertions below could be tested.

## 2. Completeness test

*Is every source item represented in the ledger?*

**Two failures.**

| Date | Statement item | Amount | In ledger? |
|---|---|---|---|
| 06/12 | Account maintenance fee | -175.00 | **No** |
| 06/22 | Interest credit | 40.00 | **No** |

Both occurred at the institution and were never recorded. Neither is a timing difference: the institution has already applied them.

## 3. Validity test

*Is every ledger item supported by a source item?*

**One failure.**

| Date | Ledger item | Amount | Supported by source? |
|---|---|---|---|
| 06/18 | Vendor payment, reference V-3310 | -135.00 | **No** |

The statement shows no payment matching this reference in the period. This is **not** classified as an unpresented payment, because the operator's outstanding-items list does not include it and no supporting document was provided. Its basis is unknown.

## 4. Reconciling-item schedule

| Item | Arose | Age at 06/30 | Amount | Classification | Basis |
|---|---|---|---|---|---|
| Deposit, tenant receipt | 06/29 | 1 day | 8,500.00 | Timing | Operator reports clearing first business day of July |
| Check #1042, Contractor Co | 06/26 | 4 days | -3,200.00 | Timing | Issued, not yet presented |
| **Check #0987, Supplier Co** | **02/14** | **136 days** | **-1,250.00** | **Timing, but aged** | Still unpresented after more than four months |
| Account maintenance fee | 06/12 | 18 days | -175.00 | **Unexplained** | Applied by the institution, never recorded |
| Interest credit | 06/22 | 8 days | 40.00 | **Unexplained** | Applied by the institution, never recorded |
| Vendor payment V-3310 | 06/18 | 12 days | -135.00 | **Unexplained** | In the ledger, no source support |

**Check #0987 is flagged despite its classification.** An item outstanding for 136 days is a finding regardless of size. Checks that never present eventually raise questions of staleness and escheatment, which are outside this pack. No aging threshold was provided *(missing)*, so it is reported against ordinary expectation rather than an office rule.

## 5. Gross movement summary

**Stated gross, before any netting.**

| Direction | Items | Gross |
|---|---|---|
| Items that would increase the ledger balance | Interest credit 40.00; V-3310 reversal 135.00 | 175.00 |
| Items that would decrease the ledger balance | Maintenance fee 175.00 | 175.00 |
| **Net effect of unexplained items** | | **0.00** |

**Gross unexplained movement: 350.00. Net: 0.00.**

The formal reconciliation also nets to zero:

| | Amount |
|---|---|
| Statement balance, June 30 | 138,135.00 |
| Add: deposit in transit | 8,500.00 |
| Less: check #1042 | (3,200.00) |
| Less: check #0987 | (1,250.00) |
| **Adjusted statement balance** | **142,185.00** |
| Ledger balance, June 30 | 142,185.00 |
| **Difference** | **0.00** |

> The difference is zero **because three errors offset**, not because the account is correct. This is the failure mode the two assertions exist to expose.

## 6. What a person must still resolve

1. **Record or explain the maintenance fee, 175.00.** The institution has taken it. The ledger does not reflect it.
2. **Record or explain the interest credit, 40.00.** Same, in the other direction.
3. **Establish what V-3310 is.** A 135.00 ledger payment with no source support is either a payment the institution never processed, a duplicate, or an entry made against the wrong account. Each has a different remedy.
4. **Decide the treatment of check #0987** after 136 days outstanding.
5. **Confirm the operator's outstanding-items representation**, which is currently the only support for classifying the deposit and check #1042 as timing.
6. **Reach a conclusion.** This pack contains none.

## 7. Gaps, assumptions, and limits

- **No aging threshold provided** *(missing)*. Check #0987 is flagged on ordinary expectation, not an office rule.
- **Outstanding items are an operator representation** *(assumption)*, not independently evidenced. If the deposit did not in fact clear in early July, its timing classification is wrong.
- **Scope covered:** the Operating account only, June 1 to June 30. Nothing here tests any other account, entity, or period.
- **Prior reconciling items are partially independent** at best, since they were carried from prior reconciliations rather than re-evidenced.
- **No conclusion is stated, and none should be inferred** from the zero difference in section 5.

---

*This pack is unverified evidence assembled for human review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It does not reconcile the account, does not conclude that the balance ties, and does not sign off. The reconciliation, the conclusion, and the sign-off are the responsibility of a competent person.*
