# Family Office AI Skills

**Reusable AI workflows for lean family offices, RIAs, and wealth operators.**

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)
![Status: v1](https://img.shields.io/badge/status-v1-informational.svg)
![Made for](https://img.shields.io/badge/made%20for-family%20offices%20·%20RIAs%20·%20wealth%20operators-0b3d2e.svg)

An open-source library of structured **AI skills, prompts, and workflow templates** for single-family offices, multi-family offices, registered investment advisers (RIAs), and the operators who run them — chiefs of staff, investment analysts, executive assistants, and operations teams. Each skill is a repeatable workflow with defined inputs, output structure, and guardrails, not a one-off prompt. Everything is read-only and judgment-supporting: nothing here decides, transacts, or sends.

> **Important.** These materials support human judgment; they do not replace it. They are not investment, legal, tax, accounting, compliance, or cybersecurity advice, and their use creates no professional, advisory, or fiduciary relationship. Every output is an unverified draft for human review. See the [Disclaimer](#disclaimer) before use.

---

## Contents

- [Try this first](#try-this-first)
- [For advanced operators and builders](#for-advanced-operators-and-builders)
- [Why this exists](#why-this-exists)
- [What's inside](#whats-inside)
- [The skills](#the-skills)
- [Who it's for](#who-its-for)
- [How to use these skills](#how-to-use-these-skills)
- [Examples in practice](#examples-in-practice)
- [Documentation](#documentation)
- [Trust and safety posture](#trust-and-safety-posture)
- [Privacy, security, and governance](#privacy-security-and-governance)
- [Disclaimer](#disclaimer)
- [Built from operator experience](#built-from-operator-experience)
- [Contributing](#contributing)
- [License](#license)

---

## Try this first

New here? The [Quickstart](QUICKSTART.md) walks you through running one skill in under five minutes.

- **Start with [Principal Weekly Brief](skills/principal-weekly-brief/)** — the simplest, highest-frequency workflow to see how a skill behaves.
- **Use fictional or approved, non-confidential data** — never paste confidential information into public or unapproved AI tools.
- **Treat the output as a draft for human review** — verify every fact against source before relying on it.

## For advanced operators and builders

This repository treats AI adoption as an operating-system problem, not a prompt-engineering problem. If you are designing an AI-native family office operating layer — as an RIA COO, chief of staff, or wealthtech builder — start here:

- **[Reference architecture](docs/reference-architecture.md)** — the six-layer model: context, connector governance, skills, review gates, outputs, measurement.
- **[AI Workforce operating model](docs/ai-workforce-operating-model.md)** — what an AI Workforce is, what stays human, and the vocabulary (prompt → skill → workflow → system).
- **[Skill maturity matrix](docs/skill-maturity-matrix.md)** — how usage matures from a one-off prompt to an operating layer (more structure and review, not more autonomy).
- **[System blueprints](blueprints/)** — composed, end-to-end designs (briefing, opportunity review, meeting-to-execution, vendor management).
- **[Evaluation examples](evals/)** — non-executable red-team scenarios for testing conservative behavior.
- **[Connector / context-access guide](docs/connectors-and-context.md)** — how approved context enters workflows, as a governed data-access risk.

## Why this exists

A lean family office runs on a small team carrying a wide surface area: investments, operations, governance, communications, reporting, vendors, entities, travel, and the principal's time. Headcount rarely scales with complexity. The constraint is almost always attention, not ambition.

An **AI-native family office** treats AI as an operating layer that absorbs the repeatable, structure-heavy work — drafting briefs, screening deals, summarizing diligence, preparing meetings, extracting action items, digesting documents — so that scarce human judgment is spent where it matters. The goal is **operating leverage**: a small team preparing more thoroughly and following through more reliably, with a person accountable for every judgment. AI does not reduce the office's risk; used carelessly it adds risk, which is why governance and human review are central to everything here.

**These are workflows, not prompts.** A prompt is a sentence; a workflow is a contract. Each skill specifies the inputs it expects, the output structure it produces, the behavioral rules it must follow, the quality-control checks it runs against itself, and the things it must never do. That structure makes output more consistent and easier to review — it does not make the output correct, so verification by a competent person remains required. It is also what separates this from generic "prompt engineering."

This repository publishes generalized, sanitized versions of workflows that map to that operating model. They contain no real names, entities, deals, vendors, principals, or data, and are meant to be read, adapted, and run inside your own governed environment.

## What's inside

```
family-office-ai-skills/
├── skills/        Seven structured AI workflows (SKILL.md + README + examples)
├── templates/     Reusable markdown templates for the artifacts they produce
└── docs/          Governance, privacy, implementation, and operating-model guidance
```

- **`skills/`** — Seven workflows. Each contains a `SKILL.md` (the workflow contract), a `README.md` (plain-English overview), and an `examples/` folder with a fictional sample input and the resulting output.
- **`templates/`** — Reusable markdown templates for weekly briefs, investment memos, manager diligence, meeting prep, and action items.
- **`docs/`** — Practical guidance for running AI responsibly inside a family office or RIA: [governance](docs/ai-governance-for-family-offices.md), [privacy](docs/privacy-and-confidentiality.md), [implementation](docs/implementation-guide.md), and the [operating model](docs/operating-model.md).

## The skills

| Skill | What it does | Example use case |
|-------|--------------|------------------|
| [Principal Weekly Brief](skills/principal-weekly-brief/) | Turns the week's calendar, decisions, and updates into a concise principal briefing | A chief of staff drafts the weekly brief in a consistent format for review |
| [Investment Memo Screener](skills/investment-memo-screener/) | Converts a deal summary, deck, CIM excerpt, or founder email into a first-pass investment memo | An analyst triages inbound deal flow into a consistent screening format |
| [Manager Diligence Summarizer](skills/manager-diligence-summarizer/) | Summarizes fund and manager materials into a diligence-ready format | An RIA standardizes manager write-ups across an allocation pipeline |
| [Meeting Prep Pack](skills/meeting-prep-pack/) | Builds a structured meeting brief from prior notes, attendees, and agenda | An EA prepares the principal for a counterparty meeting |
| [Post-Meeting Action Extractor](skills/post-meeting-action-extractor/) | Converts raw meeting notes into decisions, owners, and deadlines | An operator turns a long meeting into a clean, owned action list |
| [Vendor Review](skills/vendor-review/) | Evaluates vendor proposals, renewals, and service issues | An ops lead reviews a custodian or technology renewal before approval |
| [Document Digest](skills/document-digest/) | Summarizes legal, insurance, trust, or operating documents into plain English | An operator gets a plain-English read of a subscription doc before it goes to counsel |

## Who it's for

This library is built for two audiences that rarely share a vocabulary. It is written so both can use it.

**Family office and wealth management operators**
Single-family and multi-family office operators, RIAs, investment analysts, chiefs of staff, executive assistants, and wealth operations teams. If you prepare briefings, screen deals, run diligence, manage vendors, or turn meetings into follow-through, these are the workflows you already do by hand — made repeatable.

**AI builders and agent developers**
Engineers and operators building AI assistants, agents, and internal tooling for wealth and finance. Each `SKILL.md` is a clean, model-agnostic specification — structured inputs, defined output schema, explicit guardrails — that you can adapt into a skill file, a system prompt, or a step in an agent workflow. The format is compatible with skill-based agent runtimes and works with any capable assistant that follows structured instructions.

## How to use these skills

These skills are **model-agnostic**. They work with any capable AI assistant that can follow a structured instruction set — a general-purpose assistant or an agent runtime that supports skill files.

1. **Choose a skill** that matches the task in front of you.
2. **Open its `SKILL.md`** and read the *Inputs*, *Output*, and *Do not* sections.
3. **Gather the inputs** the skill asks for. Provide only sanitized material — see [privacy guidance](docs/privacy-and-confidentiality.md).
4. **Invoke the skill** by giving the AI the instruction set plus your inputs (see each skill's *Example request*).
5. **Review the output as a draft.** Every output is a starting point for a human, never a final decision. Verify all facts against source.
6. **Adapt the templates** in [`templates/`](templates/) to match your house style and recordkeeping.

For a full rollout — pilot selection, training, and review loops — see the [Implementation Guide](docs/implementation-guide.md).

## Examples in practice

Each skill ships with a fictional, end-to-end example so you can see exactly what goes in and what comes out.

- **Investment Memo Screener** — *In:* a cold founder email raising a seed round. *Out:* a structured first-pass memo that separates the promoter's thesis from verified fact, lists specific diligence questions, and flags the missing financials and terms — making no recommendation to invest.
  → [sample input](skills/investment-memo-screener/examples/sample-input.md) · [sample output](skills/investment-memo-screener/examples/sample-output.md)

- **Post-Meeting Action Extractor** — *In:* raw, messy operations-review notes. *Out:* clean decisions, owners, and deadlines, with every missing owner or date explicitly flagged rather than guessed, plus an internal follow-up draft a person reviews and sends.
  → [sample input](skills/post-meeting-action-extractor/examples/sample-input.md) · [sample output](skills/post-meeting-action-extractor/examples/sample-output.md)

- **Document Digest** — *In:* a dense fund subscription excerpt. *Out:* a plain-English summary, the key dates and obligations, unusual terms flagged for review, and the precise questions to put to counsel — without giving legal advice.
  → [sample input](skills/document-digest/examples/sample-input.md) · [sample output](skills/document-digest/examples/sample-output.md)

Browse any skill's `examples/` folder for the rest.

## Documentation

| Guide | What it covers |
|-------|----------------|
| [AI Governance for Family Offices](docs/ai-governance-for-family-offices.md) | Approved and prohibited use cases, model selection, human review, recordkeeping, staff training, accountability |
| [Privacy and Confidentiality](docs/privacy-and-confidentiality.md) | What must never be pasted into public tools, de-identification, failure modes, a pre-paste checklist |
| [Implementation Guide](docs/implementation-guide.md) | A step-by-step rollout for a small office or RIA: pilot selection, training, review loops, measurement |
| [Operating Model](docs/operating-model.md) | The eight-layer AI-native family office operating model, from information intake to executive decision support |
| [Reference Architecture](docs/reference-architecture.md) | The six-layer AI-native family office architecture: context, connector governance, skills, review gates, outputs, measurement |
| [AI Workforce Operating Model](docs/ai-workforce-operating-model.md) | What an "AI Workforce" is and is not, the prompt→skill→system vocabulary, and what stays human |
| [Skill Maturity Matrix](docs/skill-maturity-matrix.md) | How AI usage matures from a one-off prompt to an operating layer — more structure and review, not more autonomy |
| [Connectors and Context Access](docs/connectors-and-context.md) | How an optional context-access layer fits, its maturity levels, and an approval checklist — a data-access risk, not a safety control |
| [Threat Model](docs/threat-model.md) | Practical risks of public family office AI skills, misuse cases, and the human-review model |
| [Evaluation and Red-Team Guide](docs/evaluation-guide.md) | How to test that a skill behaves conservatively, with example red-team prompts and expected safe responses |
| [Measurement Framework](docs/measurement-framework.md) | Honest, directional metrics for adoption and value — with explicit limits |
| [AI Maturity Model](docs/family-office-ai-maturity-model.md) | Five levels from no formal AI use to a governed, AI-native family office |
| [Skill Design Principles](docs/skill-design-principles.md) | The rules every skill in this library follows |
| [Operator Case Study](docs/operator-case-study.md) | Sanitized example of measuring an AI-native family office workflow layer (illustrative figures) |

**System blueprints:** composed, end-to-end designs in [`blueprints/`](blueprints/) — [weekly principal briefing](blueprints/weekly-principal-briefing-system.md), [investment opportunity review](blueprints/investment-opportunity-review-system.md), [meeting-to-execution](blueprints/meeting-to-execution-system.md), and [vendor management](blueprints/vendor-management-system.md).

**Evaluation examples:** non-executable red-team scenarios in [`evals/`](evals/) for testing that a skill behaves conservatively under pressure.

For AI builders: the machine-readable [skill catalog](skills/catalog.yaml) and its [JSON schema](schemas/skill-manifest.schema.json) document each skill's conservative metadata. See the [Roadmap](ROADMAP.md) for direction and the [Changelog](CHANGELOG.md) for history.

## Trust and safety posture

The short version of how this library is meant to be used:

- **Skills are read-only by default** — they draft, summarize, and structure; they do not act.
- **No skill grants transaction authority** — nothing here approves, executes, allocates, or sends.
- **Human review is required** — every output is an unverified draft for a competent person to verify.
- **Guardrails are instructions, not guarantees** — a skill's rules are written instructions to the AI, not enforceable controls; human review is the real control.
- **Connectors are a data-access risk, not a safety control** — connectors may improve context, but they should be approved, scoped, and treated as a data-access risk, not a safety control.
- **You are responsible for professional review and compliance** — these materials are not investment, legal, tax, accounting, compliance, cybersecurity, or fiduciary advice, and create no professional relationship.

See the [Threat Model](docs/threat-model.md) and [Evaluation Guide](docs/evaluation-guide.md) for how this posture is maintained in practice.

## Privacy, security, and governance

AI tools introduce real confidentiality and governance risk if used carelessly. Before using anything here:

- **Do not paste confidential family or client information into public or consumer AI tools.** Use an enterprise environment with appropriate data-handling terms. See [Privacy and Confidentiality](docs/privacy-and-confidentiality.md).
- **Keep a human in the loop.** These skills support judgment; they do not replace it. Nothing here should approve, commit, transact, or send on its own.
- **Govern your usage.** Define approved and prohibited use cases, model selection, review requirements, and recordkeeping before you scale. See [AI Governance for Family Offices](docs/ai-governance-for-family-offices.md).
- **Verify every fact.** AI output can be confidently wrong. Treat all figures, dates, names, and claims as unverified until a human confirms them against source documents.
- **Guardrails are instructions, not guarantees.** The rules inside each skill — its *Do not* list and quality-control checks — are written instructions to the AI, not technical controls. A model may not follow them perfectly. Human review, not the prompt, is the real control that keeps an unsafe output from becoming an unsafe action.

See [SECURITY.md](SECURITY.md) for how to report a concern.

## Disclaimer

This repository is provided for general informational and operational purposes only. **It is not, and must not be relied upon as, investment, legal, tax, accounting, compliance, or cybersecurity advice.** The skills and templates do not constitute a recommendation to make, hold, or dispose of any investment, or to take any other action.

AI-generated output can be inaccurate, incomplete, or misleading. You are responsible for independently verifying all output and for obtaining advice from qualified professionals before acting. Use of anything in this repository is entirely at your own risk, and you are responsible for your own professional review, supervision, and regulatory compliance. Use of these materials creates no attorney-client, adviser, fiduciary, or other professional relationship, and nothing here is tailored to your specific circumstances. See [LICENSE](LICENSE) for the full disclaimer of warranties and limitation of liability.

## Built from operator experience

Created by Greg Jones from generalized operator experience. The repository contains sanitized workflow patterns and fictional examples. It is an independent public project and is **not affiliated with, endorsed by, or representative of any employer, client, principal, family office, investment adviser, or other third party.**

The workflows describe general patterns for lean family office and wealth operations — briefings, screening, diligence, meeting prep, follow-through, and document digestion. They are shared so other operators can adapt the *structure*, not to prescribe any particular decision or to publish any private operating system.

## Contributing

Contributions are welcome — additional skills, sharper guardrails, improved templates, and clearer documentation. Good contributions make these workflows safer and more useful in real operating environments.

Every contribution must contain **no confidential or client-specific information, no live credentials, and no investment, legal, or tax advice**, and must maintain a professional, institutional tone. New skills should follow the standard `SKILL.md` format and ship with a sanitized, fully fictional example.

Start with [CONTRIBUTING.md](CONTRIBUTING.md) for the full guidelines and the new-skill checklist. If you find content that overclaims, reads as advice, or could expose sensitive information, please open an issue — that kind of review is as valuable as new material.

## License

Released under the [MIT License](LICENSE). You are free to use, modify, and distribute these materials, including commercially, provided the license and copyright notice are retained. The software and content are provided "as is," without warranty of any kind. **You remain responsible for your own professional review, supervision, and regulatory compliance.**

---

<sub>Topics: family-office · single-family-office · multi-family-office · wealth-management · ria · registered-investment-adviser · ai-agents · ai-skills · prompt-library · workflow-templates · investment-operations · due-diligence · chief-of-staff · fintech · wealthtech</sub>
