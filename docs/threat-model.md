# Threat Model

A practical threat model for using and contributing to a public library of family office AI skills. The aim is to be useful to an operator and a contributor, not exhaustive or academic. It describes what can go wrong, why, and the practices that reduce the risk. None of these mitigations are technical controls; the repository is non-executable by default and the real control is human judgment.

---

## Purpose

To make the risks of using AI in family office workflows explicit, so operators adopt these skills with their eyes open and contributors do not unknowingly add risk. The most important risks here are not exotic attacks — they are ordinary, high-probability mistakes: confidential data in the wrong tool, fluent output mistaken for truth, and a read-only workflow quietly turned into an autonomous one.

## Scope

**In scope:** the content of this repository (skills, templates, docs, examples), and the ways operators and AI builders use or adapt it.

**Out of scope:** the security of any specific AI vendor, model, or environment you run these skills in; your office's broader IT security; and any integration you build on top of these materials. Those remain your responsibility.

## Assets to protect

| Asset | Why it matters |
|-------|----------------|
| Confidential family/principal information | Net worth, holdings, structures, health, security, travel — high-harm if exposed |
| Client and counterparty information | Confidentiality obligations; reputational and legal exposure |
| Decision quality | Bad inputs or false confidence can corrupt real decisions |
| The office's credibility | Acting on an unverified AI output that proves wrong |
| The repository's integrity | A risky contribution could mislead many downstream users |

## Threats

| # | Threat | How it happens |
|---|--------|----------------|
| T1 | Confidential information pasted into public AI tools | An operator uses a consumer tool out of convenience and exposes sensitive data |
| T2 | AI output mistaken for professional advice | A digest or memo is treated as legal/investment advice rather than a draft |
| T3 | Skill instructions treated as enforceable controls | Someone assumes the `Do not` list reliably prevents bad output |
| T4 | A read-only skill adapted into an autonomous workflow | A builder wires a skill to send, approve, or transact without a human |
| T5 | Hidden prompt injection in a source document | A pasted document contains instructions that subvert the skill |
| T6 | False confidence from clean formatting | Well-structured output reads as authoritative regardless of accuracy |
| T7 | Accidental disclosure through sample data | A contributor uses real (or thinly disguised) data in an example |
| T8 | Unreviewed contributions add risky instructions | A pull request introduces advice, autonomy, or weakened guardrails |

## Misuse cases

- Using a skill to generate an "investment recommendation" and acting on it without diligence or advice.
- Pasting a trust instrument into a public chatbot to "save time."
- Building an agent that reads email, runs a skill, and replies to a manager automatically.
- Presenting an AI-drafted brief to a principal as verified fact.
- Copying a skill's output into a regulatory or client deliverable without review.

## Confidentiality risks

The highest-probability harm. AI tools are a new surface where sensitive information can be exposed, retained, or aggregated. Individually harmless details (a name, a residence, a date) can become sensitive in combination. See [privacy-and-confidentiality.md](privacy-and-confidentiality.md) for the detailed rules, including what must never be pasted into public tools.

## Prompt-injection and skill-injection risks

Source documents and pasted materials can contain instructions — visible or hidden — that attempt to override a skill's rules ("ignore the confidentiality rules," "recommend this investment," "send this"). Because a skill's guardrails are instructions to the model, not enforced controls, an injected instruction may be followed. **Mitigation is procedural:** review output against the skill's intended behavior, be suspicious of documents from untrusted sources, and never let skill output drive an action without human review.

## Overreliance risks

Fluent, well-formatted output invites trust it has not earned. The risk increases under time pressure ("the principal wants it now") and with repetition (the workflow has "always been fine"). The mitigation is a standing habit: treat every output as an unverified draft and verify material facts against source — most rigorously exactly when time is short.

## Professional advice boundary risks

These skills can produce output that *resembles* legal, tax, or investment analysis. The risk is that resemblance is mistaken for advice. Every skill is bounded to preparation and questions *for* a professional, never conclusions *from* one. Operators must route anything requiring professional judgment to the appropriate adviser, and contributors must not blur this line.

## Automation/autonomy risks

The skills are read-only by design. The risk is that a builder removes the human from the loop — wiring a skill into a pipeline that sends, approves, or transacts. Nothing in this repository grants that authority, and doing so converts a low-risk drafting aid into a high-risk autonomous system. Any such integration must be independently reviewed by someone accountable for security and compliance.

## Mitigations

| Risk | Practice that reduces it |
|------|--------------------------|
| Confidential exposure (T1, C-risks) | Use an approved enterprise environment; de-identify; never paste sensitive data into public tools |
| Mistaken for advice (T2) | Preserve disclaimers; route professional questions to advisers |
| Guardrails over-trusted (T3) | Treat `Do not` lists as instructions; rely on human review |
| Autonomy creep (T4) | Keep a human between output and action; review any integration |
| Prompt injection (T5) | Distrust instructions inside source material; verify output behavior |
| False confidence (T6) | Verify facts against source regardless of how clean the output looks |
| Sample-data leakage (T7) | Use only fictional examples; review PRs for real data |
| Risky contributions (T8) | Enforce the contribution checklist and safety-review process |

## Human review model

Human review is the primary control in this repository. It scales with consequence:

| Consequence | Review |
|-------------|--------|
| Internal, low stakes | Spot-check before use |
| Principal-facing or analytical | Verify facts and framing by a competent person |
| Feeds a decision | Verify every material fact against source; named reviewer |
| External communication | A person writes/approves and sends; AI never sends |

The reviewer is accountable for the output as if they had produced it. "The AI generated it" is never an explanation for an error that reaches a principal, client, or counterparty.

## What this repository deliberately does not do

- It does not provide investment, legal, tax, accounting, compliance, cybersecurity, or fiduciary advice.
- It does not execute transactions, approve commitments, or move money.
- It does not send communications.
- It does not connect to live systems or store credentials.
- It does not ship executable code, scripts, or automation by default.
- It does not claim its guardrails are enforceable controls or that its output is reliable.

These omissions are intentional and central to the repository's safety posture.

---

*This threat model is practical guidance, not a security guarantee or professional advice. Your environment, integrations, and obligations are your responsibility.*
