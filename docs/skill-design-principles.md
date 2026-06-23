# Skill Design Principles

How skills in this repository are designed. These principles keep the library consistent, conservative, and useful. Every existing skill follows them, and every new skill must. Read this alongside [CONTRIBUTING.md](../CONTRIBUTING.md) and [CLAUDE.md](../CLAUDE.md) before adding a skill.

---

## 1. Workflows, not prompts

A skill is a contract, not a sentence. It specifies inputs, an output structure, behavioral rules, quality-control checks, and prohibited actions. That structure is what makes output consistent and reviewable — and what distinguishes this from generic prompt engineering.

## 2. Read-only by default

Skills support judgment; they do not act. A skill never executes a transaction, approves a commitment, sends a communication, or connects to a live system. If a workflow would require any of those, it does not belong here in that form.

## 3. Human review is required

Every skill produces an unverified draft for a competent person to review. The skill states that review is required. The skill is never the final step before a consequential action.

## 4. No professional advice

A skill may prepare analysis, summaries, and questions *for* a professional. It must not provide investment, legal, tax, accounting, compliance, or fiduciary advice, state conclusions a professional would state, or recommend a transaction or allocation. The advice boundary is explicit in each skill.

## 5. Separate facts from assumptions

A skill distinguishes what the input confirms from what it infers. Assumptions are labeled. The reader can always tell which is which.

## 6. Surface missing information

A skill flags what it does not know rather than filling the gap. Under pressure to "just give an answer," the correct behavior is still to flag the gap, not to fabricate.

## 7. Decision-ready, not decision-making

Output should be concise, structured, and useful enough to support a decision — and must stop short of making one. The skill frames decisions for human judgment; it does not render them.

## 8. Every skill includes prohibited actions

Each `SKILL.md` has a `Do not` section listing what the skill must never do. These are written instructions to the AI, understood as guidance rather than enforceable controls — which is exactly why human review remains the real safeguard.

## 9. Every skill includes quality control

Each skill has a `Quality control` section covering, at minimum: handling of missing information, hallucination risk, confidentiality, and uncertainty. This is where the skill tells the AI how to check itself.

## 10. Every skill includes a sample input and sample output

Each skill ships with `examples/sample-input.md` and `examples/sample-output.md`. The sample output models conservative behavior: facts separated from assumptions, missing information flagged, no advice, no recommendation, disclaimer intact.

## 11. Sample data must be fictional

All examples use fully fictional, generic data — no real names, entities, deals, vendors, principals, or figures, and nothing thinly disguised. Placeholders (`[Principal]`, `[Entity A]`, "the Fund") are preferred.

## 12. Carry the disclaimer

Each skill includes a closing disclaimer making clear it supports judgment, gives no professional advice, authorizes no action, and requires human verification. Disclaimers are preserved, never weakened.

---

## The standard `SKILL.md` structure

```
---
name: <kebab-case-id>
description: <when to use and what it produces>
---

# <Display Name>

## Purpose
## When to use this
## Inputs
## Output
## Instructions
## Quality control
## Do not
## Example request

---
<disclaimer footer>
```

A skill that follows these principles will read like the rest of the library: conservative, structured, and clearly bounded.

---

*These principles are operational guidance for designing skills. They are not professional advice, and following them does not make any AI output reliable — human review remains required.*
