# Pre-Booking Gap Analysis

**Entity:** Operating LLC
**Account:** Operating account
**Period:** March 1 to March 31
**Prepared by:** [Preparer]
**Date:** [Date]
**Status:** Draft for review. Nothing below has been booked.

> Classifications are drawn from the material provided and are unverified. Items marked *(assumption)* are inferred; items marked *(missing)* were not provided. The draft entry packet covers only the genuinely missing population. A person must verify every classification against source records before anything is recorded.

**Comparison basis.** Compared 12 source items against 6 ledger entries for the operating account, March 1 to March 31, ledger extract as-of March 31. Dates matched on posting date; amounts matched to the cent; descriptions were normalized to lower case with punctuation removed. No office tolerance was provided, so no variance was treated as acceptable *(missing)*.

---

## 1. Coverage summary

| Classification | Items | Amount |
|---|---|---|
| Already booked | 4 | 32,838.00 |
| Partially booked | 1 | 2,240.00 |
| Covered by aggregate | 2 | 2,487.45 |
| Pending | 1 | 5,000.00 |
| Duplicate representation | 1 | 143.20 |
| Genuinely missing | 2 | 7,643.20 |
| Ambiguous | 1 | 15,000.00 |
| **Total** | **12** | **65,351.85** |

Counts sum to the 12-item source population and amounts sum to the source total of 65,351.85.

**Both directions:**

| | Amount |
|---|---|
| Source total | 65,351.85 |
| Ledger total | 37,529.45 |
| Difference | 27,822.40 |

That difference is fully explained: 7,643.20 genuinely missing, 15,000.00 ambiguous, 5,000.00 pending, 36.00 partial-booking variance, and 143.20 of duplicate representation that is not an economic event. Those five sum to 27,822.40. **The draft packet closes only 7,643.20 of it.**

## 2. Classification detail

| # | Date | Description | Amount | Classification | Evidence |
|---|------|-------------|--------|----------------|----------|
| 1 | 03/02 | Insurance premium | 4,150.00 | Already booked | JE-1041, same date and amount |
| 2 | 03/03 | Software subscription | 288.00 | Already booked | JE-1042, same date and amount |
| 3 | 03/05 | Landscaping service | 1,875.00 | Covered by aggregate | Inside JE-1058 batch; 1,875.00 + 612.45 = 2,487.45 |
| 4 | 03/07 | Transfer to reserve | 25,000.00 | Already booked | JE-1049, same date and amount |
| 5 | 03/09 | Utility payment | 612.45 | Covered by aggregate | Inside JE-1058 batch, as above |
| 6 | 03/12 | Property management fee | 3,400.00 | Already booked | JE-1055, same date and amount |
| 7 | 03/14 | Office supplies, settled | 143.20 | **Genuinely missing** | No ledger entry at this date or amount, and not within any batch |
| 8 | 03/14 | Office supplies, pending | 143.20 | Duplicate representation | Same amount, date, and description as item 7; pending authorization for the settled charge |
| 9 | 03/18 | Legal services | 7,500.00 | **Genuinely missing** | No ledger entry at this date or amount, and not within any batch |
| 10 | 03/22 | Repairs, residence | 2,240.00 | Partially booked | JE-1061 same date, booked 2,204.00, variance 36.00 |
| 11 | 03/27 | Outgoing wire "REF 88213" | 15,000.00 | Ambiguous | No payee shown; cannot determine nature or counterparty |
| 12 | 03/29 | Equipment deposit | 5,000.00 | Pending | Not settled as of the period end |

## 3. Genuinely missing

The only population eligible for a draft entry.

| # | Date | Description | Amount |
|---|------|-------------|--------|
| 7 | 03/14 | Office supplies, card purchase | 143.20 |
| 9 | 03/18 | Legal services | 7,500.00 |

**Total: 7,643.20**

## 4. Requires a person

| # | Item | Amount | Question to resolve |
|---|------|--------|---------------------|
| 10 | Repairs, residence | Variance 36.00 | JE-1061 was booked at 2,204.00 against a source amount of 2,240.00. The digits are transposed, which is consistent with a keying error, but it could also be a deliberate split or a partial payment. Which is it, and should the entry be corrected or supplemented? |
| 11 | Outgoing wire "REF 88213" | 15,000.00 | The memo carries no payee and the reference is not resolvable from the material provided. Who was paid, and what was the purpose? Until that is known, no account code can be selected. |
| 12 | Equipment deposit | 5,000.00 | Pending at period end. Confirm whether the office books pending items in the period authorized or the period settled. No policy was provided *(missing)*. |
| 8 | Office supplies, pending | 143.20 | Confirm this is the authorization for the settled charge in item 7 and not a second purchase of the same amount on the same day. If confirmed, it is not a separate economic event. |

## 5. Draft entry packet

For the genuinely missing items only. Account codes are **not** proposed, because no chart of accounts was provided *(missing)*.

**Draft 1**
- Date: 03/14
- Description: Office supplies, card purchase
- Amount: 143.20
- Debit: [expense account to be selected by the office] *(missing)*
- Credit: Operating account
- Support: source item 7

**Draft 2**
- Date: 03/18
- Description: Legal services
- Amount: 7,500.00
- Debit: [expense account to be selected by the office] *(missing)*
- Credit: Operating account
- Support: source item 9

**Packet total: 7,643.20**

## 6. Gaps and assumptions

- **No chart of accounts provided** *(missing)*. Draft entries name no account codes. They are incomplete until the office supplies them.
- **No matching tolerance provided** *(missing)*. Item 10 is reported as a variance rather than an acceptable difference, because no threshold exists to judge it against.
- **No pending-item policy provided** *(missing)*. Item 12 is not classified as missing, since whether it belongs in this period is a policy question.
- **JE-1058 composition is inferred** *(assumption)*. The batch amount equals the sum of items 3 and 5 exactly, which is strong but not conclusive. If the batch actually contains different components that happen to sum to the same figure, items 3 and 5 would be genuinely missing and the packet would be understated by 2,487.45. Confirm the batch detail before relying on this.
- **Single account, single period.** No cross-account review was performed, so a transfer whose other leg sits in a different account would not have been detected here. Run the transfer and duplicate review if the period spans several accounts.

---

*This analysis is an unverified draft for human review. It is not accounting, tax, audit, or financial advice, and creates no professional relationship. It books no entry, reconciles no account, and closes no period. Every classification and every draft entry must be verified against source records by a competent person before anything is recorded.*
