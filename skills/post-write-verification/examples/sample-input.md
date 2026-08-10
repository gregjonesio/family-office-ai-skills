# Sample Input: Post-Write Verification

*Fully fictional. No real entity, account, system, entry, or identifier. Amounts and references are invented for illustration.*

---

**Entity:** Operating LLC
**System of record:** the office's accounting platform
**Recorded by:** [Preparer], via the entry interface
**Approved by:** [Reviewer], April 2, batch of 5 entries

---

## The approved change (what was supposed to be recorded)

| Ref | Date | Description | Debit | Credit | Amount |
|-----|------|-------------|-------|--------|--------|
| E-1 | 04/01 | Insurance expense | Insurance expense | Operating account | 4,150.00 |
| E-2 | 04/01 | Legal services | Legal expense | Operating account | 7,500.00 |
| E-3 | 04/01 | Repairs, residence | Repairs expense | Operating account | 2,240.00 |
| E-4 | 04/01 | Software subscription | Software expense | Operating account | 288.00 |
| E-5 | 03/31 | Accrued utilities, March | Utilities expense | Accrued liabilities | 612.45 |

**Batch total: 14,790.45**

## Approval record

- Approver: [Reviewer]
- Approved: April 2
- Object approved: the five entries listed above, as a batch
- No changes were noted between approval and recording.

## What the system reported

All five entries returned success with a status of `recorded`:

| Ref | Returned identifier | Status |
|-----|--------------------|--------|
| E-1 | R-8801 | recorded |
| E-2 | R-8802 | recorded |
| E-3 | R-8803 | recorded |
| E-4 | R-8804 | recorded |
| E-5 | R-8805 | recorded |

No errors were raised.

---

## Read-back evidence

**Source:** report export, "Operating account activity"
**Obtained through:** the reporting module, not the entry interface
**Scope:** Operating account only, April 1 to April 30
**As-of:** April 3, 09:15

| Date | Description | Amount | Reference |
|------|-------------|--------|-----------|
| 04/01 | Insurance expense | 4,150.00 | R-8801 |
| 04/01 | Repairs expense | 2,204.00 | R-8803 |
| 04/01 | Software expense | 288.00 | R-8804 |
| 04/01 | Software expense | 288.00 | R-8804-2 |

**Rows returned: 4. Export total: 6,930.00**
