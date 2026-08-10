# Sample Input: Transfer and Duplicate Review

*Fully fictional. No real entity, account, institution, counterparty, or transaction. Amounts and references are invented for illustration.*

---

**Period:** May 1 to May 31
**Settlement window:** up to 2 business days
**Amount tolerance:** not set by the office
**Fee conventions:** not documented by the office

## Account and entity map

| Account | Entity |
|---------|--------|
| Operating account | Operating LLC |
| Reserve account | Operating LLC |
| Property account | Property LLC |

*The office has other entities. Their accounts were not provided for this run.*

---

## Operating account (Operating LLC)

| Date | Description | Amount | Status |
|------|-------------|--------|--------|
| 05/04 | Transfer out to reserve | -25,000.00 | Settled |
| 05/07 | Payment, Landscaping Co | -3,500.00 | Settled |
| 05/11 | Outgoing wire, memo "to property" | -40,000.00 | Settled |
| 05/18 | Card authorization, Harbor Restaurant | -862.40 | Pending |
| 05/19 | Card purchase, HARBOR RESTAURANT | -879.65 | Settled |

## Reserve account (Operating LLC)

| Date | Description | Amount | Status |
|------|-------------|--------|--------|
| 05/04 | Transfer in | 25,000.00 | Settled |
| 05/26 | Withdrawal, memo "REF 4471" | -12,000.00 | Settled |

## Property account (Property LLC)

| Date | Description | Amount | Status |
|------|-------------|--------|--------|
| 05/08 | Payment, Roofing Co | -3,500.00 | Settled |
| 05/12 | Deposit, memo "funding" | 39,975.00 | Settled |
| 05/21 | Payment, Utility Co | -6,300.00 | Settled |

**Total rows provided: 10**
