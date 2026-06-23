# Privacy and Confidentiality

Family offices hold some of the most sensitive information that exists about a family: net worth, holdings, entity structures, account details, health, security arrangements, philanthropy, and personal matters. AI tools are powerful, but they are also a new place where that information can leak, persist, or be exposed. These are practical rules for handling confidential information when AI is in the loop.

The governing instinct: **share the least, in the safest place, and assume anything you paste could persist.**

---

## 1. Know what you are protecting

Treat the following as confidential by default. The more of these a piece of information touches, the more carefully it must be handled.

- Names of the family, principals, household members, and staff
- Net worth, balances, holdings, performance, and cash positions
- Entity names, structures, ownership, and governance details
- Account numbers, custodian details, and any financial identifiers
- Trust, estate, and beneficiary information
- Legal matters, disputes, and settlement terms
- Health, medical, and personal information
- Travel plans, residences, and physical-security details
- Counterparty, vendor, and deal information shared in confidence
- Passwords, API keys, tokens, and any credential

## 2. What should never be pasted into public or consumer AI tools

Do **not** put any of the following into a public chatbot, a free consumer AI tool, a browser extension of unknown provenance, or any environment without enterprise data-handling terms:

- Real names of the family, principals, or staff tied to financial detail
- Account numbers, balances, or holdings
- Entity ownership structures and governance specifics
- Trust and estate documents or terms
- Tax returns, financial statements, or capital account detail
- Legal documents, settlement terms, or matters under privilege
- Health or personal information
- Travel itineraries, residence addresses, or security arrangements
- Any credential, key, password, or token
- Counterparty information shared under an NDA or expectation of confidence

If you would not email it to a stranger, do not paste it into a tool whose data terms you have not verified.

## 3. Use the right environment

- **Prefer an enterprise AI environment** with written terms covering confidentiality, data retention, and a commitment not to train models on your inputs.
- **Verify the data terms before first use**, not after. If you cannot confirm how a tool handles your data, treat it as public.
- **Avoid unmanaged browser extensions and plug-ins** that route your data through third parties.
- **Keep a short list of approved tools** and route all confidential work through them.

## 4. Minimize and de-identify

Even in an approved environment, share only what the task requires.

- **Redact identifiers the task does not need.** A document digest rarely needs the family name; an account number is almost never required for analysis.
- **Generalize.** Replace "the Smith Family 2019 Irrevocable Trust" with "the Trust" when the specific name adds nothing.
- **Use placeholders** like `[Principal]`, `[Entity A]`, `[Vendor]`, `[Counterparty]` and keep the mapping outside the AI tool.
- **Split sensitive context from the working text** when you can analyze the structure without the identifying detail.

## 5. Control the output

- AI output is working material. Store it under the **same access controls** as the source documents it was built from.
- Do not forward AI output containing sensitive detail through channels you would not use for the underlying documents.
- Delete working drafts that are no longer needed, consistent with your recordkeeping obligations.

## 6. Watch the failure modes

- **Persistence.** Assume inputs may be retained somewhere. The safest assumption is that a paste is not fully reversible.
- **Aggregation.** Individually harmless details can become sensitive in combination (a residence + a travel date + a name).
- **Over-trust.** Fluent output invites you to relax. Sensitivity discipline must not relax with it.
- **Convenience drift.** The riskiest moment is a busy day when someone reaches for the fastest tool instead of the approved one.

## 7. Practical checklist before you paste

Ask, every time:

1. Is this an **approved environment** with acceptable data terms?
2. Have I **removed identifiers** the task does not need?
3. Would I be comfortable if this exact text were **exposed**?
4. Is there a **credential or key** hiding in what I am about to share? (Never share it.)
5. Where will the **output live**, and is that location appropriately controlled?

If any answer is uncertain, stop and resolve it before sharing.

## 8. When something goes wrong

If confidential information is exposed to the wrong tool or party:

- Stop using that tool for the matter immediately.
- Capture what was shared, when, and where.
- Escalate to the person accountable for the office's risk and, where appropriate, to legal or compliance counsel.
- Review how it happened and adjust the practice so it does not recur.

---

*This document is practical operational guidance, not legal or cybersecurity advice. Confidentiality, privacy, and data-protection obligations vary by jurisdiction and structure; consult qualified advisers for your specific situation.*
