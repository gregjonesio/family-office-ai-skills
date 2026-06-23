# AI Workforce Operating Model for Lean Family Offices

A definition and operating model for the idea of an "AI Workforce" in a family office context. The term sounds grand; the reality should be modest and governed. This document defines what an AI Workforce is, what it is not, and the human responsibilities it never absorbs.

> An AI Workforce is a governed set of AI-assisted workflows, agents, templates, and review practices that help a lean family office process information, prepare outputs, and manage recurring work **without giving AI independent decision-making authority.**

The phrase is useful only if it stays disciplined. An "AI Workforce" is not a team of autonomous digital employees. It is structured assistance with a human accountable at every consequential step.

---

## What an AI Workforce is

- A **governed set** of reusable workflows (skills), supporting templates, and review practices.
- A way to absorb **repeatable, structure-heavy work** — drafting, summarizing, organizing, preparing.
- A system with **human review as its primary control** and measurement to improve over time.
- **Model-agnostic and read-only by default**, run inside an approved environment.

## What an AI Workforce is not

- **Not autonomous.** It does not decide, approve, transact, or send on its own.
- **Not a decision-maker or adviser.** It prepares; people decide, and professionals advise.
- **Not a replacement for staff or counsel.** It changes how work is prepared, not who is accountable.
- **Not a guarantee of accuracy.** Output is unverified until a human verifies it.
- **Not a live integration in this repository.** Nothing here connects to real systems.

## A vocabulary: prompts, skills, workflows, agents, automations, systems

These words are often used loosely. Precision matters, because each step up the ladder adds structure and review needs — not autonomy.

| Term | What it is | Example |
|------|-----------|---------|
| **Prompt** | A single instruction to a model | "Summarize this document." |
| **Template** | A reusable structure for an artifact | The investment memo template |
| **Skill** | A workflow contract: inputs, output, rules, quality control, prohibitions | [Investment Memo Screener](../skills/investment-memo-screener/) |
| **Workflow** | A skill (or skills) run as a repeatable, reviewed process | Running the screener on every inbound deal the same way |
| **Agent** | An assistant configured to run a bounded workflow | An assistant set up to run the weekly brief from provided inputs |
| **Automation** | A scheduled or triggered helper that moves information (still reviewed; never deciding/sending on its own) | A scheduled prompt that drafts a brief for a person to review |
| **System / operating layer** | Skills + context + review gates + measurement + governance, working together | A weekly briefing system (see [blueprints](../blueprints/)) |

Higher on this ladder means **more structure, review, governance, and repeatability** — never more independent authority.

## The role of human review

Human review is the control that makes the whole model safe. It scales with consequence: spot-check for low-stakes drafts; verify facts for principal-facing work; a named reviewer for anything feeding a decision; and for external communication, a person writes or approves and sends. The reviewer owns the output as if they produced it.

## The role of connectors / context

Connectors are an optional context-access layer that can reduce manual copy/paste. They improve usefulness and enlarge risk simultaneously. They are not security controls. Default to manual input or approved, read-only, least-privilege access. See [connectors-and-context.md](connectors-and-context.md).

## The role of measurement

Measurement turns a static set of prompts into an improving system. Track activity (workflows run), governance (review completion, confidentiality incidents), and directional value — honestly, with value figures kept internal and caveated. Recurring corrections in review are signal: they usually mean an input was incomplete or a skill needs tuning. See [measurement-framework.md](measurement-framework.md).

## The role of governance

Governance is what keeps capability and control advancing together. Approved and prohibited use cases, model selection, connector governance, recordkeeping, and training are the difference between an AI Workforce that strengthens the office and one that quietly adds risk. See [ai-governance-for-family-offices.md](ai-governance-for-family-offices.md).

## How institutional memory improves over time

A lean office's memory often lives in individuals. An AI Workforce, used well, captures durable records — decisions, owners, learnings, document digests — in a consistent, reviewable form. Over time this compounds: better-structured memory makes briefs sharper, prep faster, and follow-through more reliable. The memory is only as trustworthy as the human review behind it, but when that discipline holds, the office's context stops leaking between meetings and across years.

## Why this matters for lean family offices

Lean family offices have a distinctive profile that makes structured AI assistance valuable — and makes discipline essential:

- **Broad operating surface area.** Investments, operations, governance, communications, reporting, vendors, entities, travel — on a small team.
- **Limited headcount.** Capacity rarely scales with complexity.
- **High confidentiality.** Some of the most sensitive information that exists about a family.
- **High context switching.** Operators move between unrelated domains all day.
- **Recurring knowledge work.** The same structure-heavy tasks repeat constantly.
- **Need for institutional memory.** Context is easily lost when attention is scarce.

These conditions are exactly where a governed AI Workforce helps most — and exactly where careless use does the most harm.

## What remains human

The AI Workforce never absorbs these. They stay with people, always:

- **Judgment**
- **Approvals**
- **Advice** (investment, legal, tax, accounting, compliance, cybersecurity)
- **Fiduciary decisions**
- **Relationship management**
- **Final communications**
- **Capital allocation**
- **Legal / tax / compliance determinations**

If a use of AI would touch any of these, the AI prepares and a human decides — never the other way around.

---

*This document is a conceptual and operational framework, not legal, compliance, investment, accounting, cybersecurity, or fiduciary advice. It defines a way of working; it does not provide or include any live integration. Adapt it to your structure and obligations with qualified advisers.*
