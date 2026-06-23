# AI Governance for Family Offices

A practical governance guide for using AI inside a single-family office, multifamily office, or RIA. The goal is to capture the operating leverage AI offers while controlling the confidentiality, accuracy, and conduct risks it introduces. This is operational guidance, not legal or compliance advice; adapt it with your own advisers.

Govern AI the way you would govern any other capability that touches sensitive information and supports consequential decisions: with clear boundaries, named accountability, human review, and a record of what happened.

---

## 1. Principles

1. **Human judgment is never delegated.** AI prepares, summarizes, drafts, and structures. People decide, approve, commit, and communicate.
2. **Confidentiality is the default.** Sensitive information is protected at every step, and the safe choice is always to withhold rather than expose.
3. **Output is unverified until a human verifies it.** Every figure, date, name, and claim is treated as a draft assertion until checked against source.
4. **Use is bounded and recorded.** The office knows what AI is used for, what it is not used for, and keeps a proportionate record of consequential use.
5. **The bar is institutional.** AI use should raise the quality and consistency of the office's work, not introduce sloppiness or risk.

## 2. Approved use cases

These are the kinds of work AI is well-suited to support in a family office, all under human review:

| Category | Examples |
|----------|----------|
| Drafting and summarizing | Principal briefs, meeting prep, document digests, note cleanup |
| First-pass analysis | Investment memo screening, manager diligence summaries, question sets |
| Structuring | Turning raw notes into action items, owners, and deadlines |
| Research support | Organizing publicly available information into a usable form |
| Operations | Vendor review preparation, checklist generation, process documentation |
| Communication drafting | Internal drafts prepared for human review before sending |

The common thread: the AI produces a **draft or structured artifact** that a person reviews before anything happens.

## 3. Prohibited use cases

AI must **not** be used to:

- Make or approve investment, allocation, or commitment decisions.
- Execute transactions, move money, or initiate transfers.
- Send communications to external parties automatically or without human review.
- Provide investment, legal, tax, accounting, or compliance advice that the office then relies on as if it came from a qualified professional.
- Process confidential information in public or consumer AI tools without appropriate data-handling terms.
- Make decisions about people (hiring, termination, compensation) without human ownership.
- Generate content that is presented as verified fact without a human verifying it.

When in doubt, the use case is prohibited until someone accountable approves it.

## 4. Privacy and data handling

- Use an **enterprise AI environment** with contractual terms that address confidentiality, data retention, and (where relevant) a commitment not to train on your inputs.
- **Minimize what you share.** Provide the AI only what the task requires. Redact or generalize names, account numbers, and identifiers where the task does not need them.
- **Never paste highly sensitive material into public tools.** See [privacy-and-confidentiality.md](privacy-and-confidentiality.md) for the detailed rules.
- **Control where output lives.** AI output is working material; store it under the same access controls as the source documents it summarizes.

## 5. Model selection

Choose the tool deliberately rather than by default:

- **Capability vs. sensitivity.** Match the model and environment to the sensitivity of the data and the consequence of the task. The more sensitive or consequential, the more you should favor an enterprise environment with strong data terms and the more human review you should require.
- **Data terms first.** Before sensitivity of capability, confirm the environment's data-handling, retention, and training terms are acceptable.
- **Consistency.** Standardize on a small number of approved tools so the team's practices, prompts, and review habits stay consistent and auditable.
- **Reassess periodically.** Capabilities and terms change. Revisit your approved-tools list on a regular cadence.

## 6. Human review

Define review depth by consequence:

| Consequence of the work | Required review |
|-------------------------|-----------------|
| Internal draft, low stakes | Spot-check before use |
| Principal-facing or analytical | Full review of facts and framing by a competent person |
| Anything feeding a decision | Verify every material fact against source; named reviewer |
| External communication | Human writes or approves and sends; AI never sends |

The reviewer is accountable for the output as if they had produced it themselves. "The AI wrote it" is never an explanation for an error that reaches a principal or counterparty.

## 7. Recordkeeping

Keep a proportionate record so the office can answer "what did we use AI for, and how was it reviewed?"

- Maintain a short, living list of **approved AI use cases and tools**.
- For consequential output (anything feeding an investment, governance, or external decision), retain the final reviewed artifact and note that it was AI-assisted and human-reviewed.
- Be mindful of any **regulatory recordkeeping obligations** that apply to your entity (for example, books-and-records and communications rules that may apply to an RIA). Consult your compliance adviser on how AI-assisted work fits your obligations.

## 8. Staff training

- Train every user on these boundaries before they use AI for office work — approved uses, prohibited uses, and the confidentiality rules.
- Teach the **failure modes**: confident inaccuracy ("hallucination"), stale information, and the temptation to over-trust fluent output.
- Make verification a habit, not a step people skip when busy.
- Give the team a clear escalation path: when an AI suggestion touches investment, legal, tax, or compliance questions, route it to the appropriate professional rather than acting on it.
- Refresh training as tools and practices evolve.

## 9. Roles and accountability

- **Sponsor (principal or senior operator):** owns the decision to use AI and the risk appetite.
- **AI use owner (often a chief of staff or operations lead):** maintains the approved-use list, tools, and this governance document.
- **Reviewers:** accountable for the specific output they sign off on.
- **Every user:** responsible for following the boundaries and protecting confidentiality.

## 10. Review cadence

Revisit this governance document at least annually, and whenever you adopt a new tool, take on a materially new use case, or experience a near-miss. Governance that is written once and never revisited stops matching how the office actually works.

---

*This document is general operational guidance and is not legal, compliance, or regulatory advice. Adapt it with qualified advisers who understand your specific structure and obligations.*
