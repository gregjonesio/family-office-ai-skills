# Operating Playbooks

How a lean family office executes its recurring operational responsibilities — and where AI reduces administrative burden without taking over judgment, authority, or accountability.

> **Fictionalized and illustrative.** These playbooks describe generalized operating patterns. They do **not** describe, represent, or disclose any actual family office, employer, client, principal, investment, vendor, counterparty, document, or operating environment. Nothing here is investment, legal, tax, accounting, compliance, insurance, or fiduciary advice, and using these materials creates no professional relationship. Every AI output described is an unverified draft requiring human review.

---

## What a playbook is

A **playbook** documents how a recurring operational responsibility is run inside a family office — the cadence, the information flow, the approvals, the accountability, and the review gates that keep it controlled. It is written for the person who owns the process: a COO, CIO, CFO, controller, chief of staff, or operations lead who already knows the work and wants a consistent, governed way to run it.

A playbook is **operational, not technical**. It describes the process first and treats AI as one component that absorbs repeatable, structure-heavy steps — reading documents into plain English, building checklists, drafting briefings, surfacing deadlines — while a named person stays responsible for every decision. The emphasis is on operating cadence and governance, not on models or prompting.

Each playbook follows the same structure: **Objective · Operating Problem · Typical Trigger · Frequency · Primary Stakeholders · Required Inputs · AI-Assisted Activities · Human Responsibilities · Review Gates · Outputs · Risks · Common Failure Points · Metrics · Related Skills · Related Blueprints · Related Case Studies · Related Governance Documents · Evolution Path.** The Review Gates and Common Failure Points sections carry the institutional controls — segregation of duties, dual authorization, independent verification, governance calendars — so a reader learns how the process is run safely even without using AI. Start a new playbook from [PLAYBOOK-TEMPLATE.md](PLAYBOOK-TEMPLATE.md).

## How playbooks differ from the rest of the repository

This repository has distinct layers that build on one another. Each answers a different question.

| Layer | Answers | Audience | Form |
|-------|---------|----------|------|
| **[Architecture](../docs/reference-architecture.md)** | How is the AI-native operating layer structured? | Builders, COOs designing the layer | Reference model |
| **[Governance](../docs/ai-governance-for-family-offices.md)** | What is allowed, who reviews, what is recorded? | Principals, COOs, compliance | Policy and posture |
| **[Blueprints](../blueprints/)** | How do several skills compose into one end-to-end system design? | Builders, operators designing a workflow | Design pattern |
| **Playbooks** | How is a recurring operational responsibility executed, and where does AI help? | Process owners (COO, CIO, CFO, controller) | Operating process |
| **[Skills](../skills/)** | What reusable AI workflow turns these inputs into this draft? | Operators, AI builders | Workflow contract |
| **[Case Studies](../case-studies/)** | What does one worked example look like, end to end? | Operators learning by example | Worked example |
| **[Evaluations](../evals/)** | Does a skill behave conservatively under pressure? | Builders, reviewers | Red-team scenario |

The three distinctions that matter most:

- **Playbooks vs. Skills.** A [Skill](../skills/) is a reusable AI workflow instruction set — defined inputs, an output structure, and guardrails for a single task (for example, [Document Digest](../skills/document-digest/) turns a document into plain-English notes). A playbook is the *operating process* a skill plugs into: the cadence, the people, the approvals, and the review gates around the work. One playbook usually uses several skills; one skill appears in many playbooks. Skills describe the tool; playbooks describe the job.

- **Playbooks vs. Blueprints.** A [Blueprint](../blueprints/) is a composed system *design* — how a set of skills, context sources, and review gates fit together into one end-to-end pattern. A playbook is the *standing operational responsibility* that a blueprint can support. Blueprints lean toward the builder's view of the system; playbooks lean toward the operator's view of the recurring duty. They cross-reference each other directly.

- **Playbooks vs. Case Studies.** A [Case Study](../case-studies/) walks one fictional scenario from problem to follow-through, end to end, as an illustration. A playbook is the *repeatable process* the case study is an instance of. Where a playbook and a case study share a name — capital call processing, insurance renewal — read the playbook for the standing process and the case study for the worked example.

## Suggested hierarchy

```
Architecture
   ↓
Governance
   ↓
Blueprints
   ↓
Playbooks
   ↓
Skills
   ↓
Case Studies
   ↓
Evaluations
```

Architecture and governance set the frame. Blueprints design composed systems. Playbooks document how recurring responsibilities are executed within that frame. Skills are the reusable AI workflows playbooks draw on. Case studies show worked examples, and evaluations test that the underlying skills behave conservatively.

## The playbooks

| Playbook | Operating responsibility | Primary owner |
|----------|--------------------------|---------------|
| [Principal Weekly Review](principal-weekly-review.md) | Consolidate the week into one reviewable briefing | Chief of staff |
| [Capital Call Processing](capital-call-processing.md) | Capture, approve, and pay a capital call without error | Controller / operations |
| [Investment Opportunity Intake](investment-opportunity-intake.md) | Triage inbound opportunities before they consume diligence time | CIO / investment analyst |
| [Board & Committee Meeting Preparation](board-meeting-preparation.md) | Prepare materials and follow-through for governance meetings | Chief of staff / COO |
| [Executive Travel Coordination](executive-travel-coordination.md) | Plan, brief, and track principal and executive travel | Executive assistant |
| [Insurance Renewal Management](insurance-renewal-management.md) | Read renewals for changes and gaps before binding | COO / operations |
| [Vendor Onboarding & Review](vendor-onboarding-and-review.md) | Onboard and periodically review service providers | Operations lead |
| [Quarter-End Close](quarter-end-close.md) | Run a controlled, on-time financial close and reporting cycle | Controller / CFO |
| [Entity Governance Calendar](entity-governance-calendar.md) | Keep entity filings, resolutions, and obligations current | COO / general counsel liaison |
| [Document Review for Counsel](document-review-for-counsel.md) | Make documents legible and route the right questions to counsel | Operations / chief of staff |

## How to use a playbook

1. **Read the Operating Problem and Review Gates first.** The point of every playbook is the judgment a person applies at the gates, not the draft the AI produces.
2. **Map the Required Inputs to your own sources.** Provide only sanitized or approved, non-confidential material — see [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md).
3. **Separate AI-Assisted Activities from Human Responsibilities.** The split is deliberate. AI reads, structures, and reminds; people decide, approve, verify, and sign.
4. **Adopt it as a pilot.** Roll one playbook out using the [Implementation Guide](../docs/implementation-guide.md) before scaling.

## A note on AI's role

AI is one component of how a sophisticated family office operates — not the operating system itself. In every playbook here, AI reduces manual reading, drafting, and tracking so scarce attention reaches the work that needs judgment. It does not decide, transact, approve, send, or advise. Guardrails written into a skill are instructions to an AI, not enforceable controls; human review at the gates is the real control. See the [AI Governance](../docs/ai-governance-for-family-offices.md), [Threat Model](../docs/threat-model.md), and [AI Workforce Operating Model](../docs/ai-workforce-operating-model.md) for the posture that holds across all of them.

---

*These playbooks are illustrative operating patterns, not legal, compliance, investment, tax, insurance, accounting, or fiduciary advice, and not live integrations. They do not approve, transact, sign, or send anything. Every output described is an unverified draft requiring human review.*
