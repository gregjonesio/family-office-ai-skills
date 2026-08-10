# Sample Input: Pre-Booking Gap Analysis

*Fully fictional. No real entity, account, vendor, or transaction. Amounts and references are invented for illustration.*

---

**Entity:** Operating LLC
**Account:** Operating account (single account, this period only)
**Period:** March 1 to March 31
**Hard date floor:** none applicable
**Matching tolerance:** not set by the office

---

## Source population (account activity, 12 items)

| # | Date | Description | Amount | Status |
|---|------|-------------|--------|--------|
| 1 | 03/02 | Insurance premium | 4,150.00 | Settled |
| 2 | 03/03 | Software subscription | 288.00 | Settled |
| 3 | 03/05 | Landscaping service | 1,875.00 | Settled |
| 4 | 03/07 | Transfer to reserve account | 25,000.00 | Settled |
| 5 | 03/09 | Utility payment | 612.45 | Settled |
| 6 | 03/12 | Property management fee | 3,400.00 | Settled |
| 7 | 03/14 | Office supplies, card purchase | 143.20 | Settled |
| 8 | 03/14 | Office supplies, authorization on 03/14 | 143.20 | Pending |
| 9 | 03/18 | Legal services | 7,500.00 | Settled |
| 10 | 03/22 | Repairs, residence | 2,240.00 | Settled |
| 11 | 03/27 | Outgoing wire, memo "REF 88213", no payee shown | 15,000.00 | Settled |
| 12 | 03/29 | Equipment deposit | 5,000.00 | Pending |

**Source total: 65,351.85**

---

## Existing ledger activity (same account, same period)

| Entry | Date | Description | Amount |
|-------|------|-------------|--------|
| JE-1041 | 03/02 | Insurance expense | 4,150.00 |
| JE-1042 | 03/03 | Software expense | 288.00 |
| JE-1049 | 03/07 | Transfer to reserve | 25,000.00 |
| JE-1055 | 03/12 | Property management | 3,400.00 |
| JE-1058 | 03/31 | March utilities and grounds, batch | 2,487.45 |
| JE-1061 | 03/22 | Repairs expense | 2,204.00 |

**Ledger total: 37,529.45**
**Ledger extract as-of date:** March 31

---

## Notes provided by the operator

- No items were previously reviewed and deliberately excluded.
- No drafts or unposted entries exist for this period.
- The office has no written tolerance for amount or date variance.
