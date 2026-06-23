# The AI-Native Family Office Operating Model

A lean family office is a small team against a wide surface area. The operating constraint is attention. An AI-native operating model treats AI as a layer that absorbs repeatable, structure-heavy work across the office so that scarce human judgment is concentrated where it actually matters: decisions, relationships, and risk.

This document describes that operating model as a set of layers. Each layer pairs a durable office function with the kind of AI support that fits it — always under human review, never autonomous. The skills in this repository map onto these layers.

---

## How to read this model

- The **layers** are functions, not software. They describe what a family office does, regardless of tools.
- Within each layer, AI plays a **support role**: intake, structuring, drafting, summarizing, surfacing. People retain every decision.
- The model is **read-only and judgment-support by design.** No layer executes transactions, sends external communications, or commits the family to anything without a human.

```
            ┌─────────────────────────────────────────┐
            │        Executive Decision Support        │   ← where judgment is spent
            ├─────────────────────────────────────────┤
            │            Institutional Memory          │   ← what the office remembers
            ├──────────┬───────────┬──────────┬────────┤
            │ Research │   Comms    │   Ops    │  Deal  │   ← the working layers
            │   &      │            │          │  Flow  │
            │ Intel    │            │          │        │
            ├──────────┴───────────┴──────────┴────────┤
            │         Analytics & Reporting            │   ← turning data into a view
            ├─────────────────────────────────────────┤
            │            Information Intake             │   ← everything coming in
            └─────────────────────────────────────────┘
```

## Layer 1 — Information intake

**Function:** Everything flowing into the office — email, documents, statements, manager updates, legal and entity paperwork, vendor notices, meeting notes, calendar items.

**The problem:** Volume and fragmentation. Important items get buried; context lives in too many places.

**AI support:** Triage and structure incoming material. Summarize documents into plain English, extract key dates and obligations, and turn raw notes into organized records — so nothing important is lost and everything is in a usable form.

**Skills that serve this layer:** [Document Digest](../skills/document-digest/), [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

**Human boundary:** People decide what matters and verify every extracted fact. AI organizes; it does not prioritize the family's interests on its own.

## Layer 2 — Research and intelligence

**Function:** Understanding opportunities, managers, markets, vendors, and counterparties well enough to support a decision.

**The problem:** Good research is time-consuming, and lean teams ration it.

**AI support:** First-pass synthesis. Convert a deal summary into a structured memo, distill manager materials into a diligence format, and organize publicly available information into a usable shape — producing a starting point an analyst can sharpen rather than a blank page.

**Skills that serve this layer:** [Investment Memo Screener](../skills/investment-memo-screener/), [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/).

**Human boundary:** AI screens and structures; it does not opine on whether to invest, and every figure and claim is verified against source before it informs a decision.

## Layer 3 — Communication

**Function:** Internal and external communication — briefs, updates, meeting preparation, follow-ups.

**The problem:** Communication is constant and consumes disproportionate operator time.

**AI support:** Draft and structure. Prepare meeting briefs, assemble principal briefings, and produce internal drafts of follow-ups — all reviewed and, where external, sent by a person.

**Skills that serve this layer:** [Meeting Prep Pack](../skills/meeting-prep-pack/), [Principal Weekly Brief](../skills/principal-weekly-brief/).

**Human boundary:** AI never sends. Every external communication is written or approved and sent by a human.

## Layer 4 — Operations

**Function:** The running of the office — vendors, service providers, renewals, processes, entity and administrative tasks.

**The problem:** Operational work is detail-heavy, recurring, and easy to let slip.

**AI support:** Prepare vendor reviews, structure renewal and service evaluations, document processes, and build checklists — turning scattered operational detail into reviewable summaries and next steps.

**Skills that serve this layer:** [Vendor Review](../skills/vendor-review/), [Document Digest](../skills/document-digest/).

**Human boundary:** AI prepares the review; people decide whether to renew, terminate, or escalate, and people execute.

## Layer 5 — Analytics and reporting

**Function:** Turning the office's data into a clear view — performance, exposures, cash, obligations, calendars.

**The problem:** Reporting is repetitive and time-sensitive, and inconsistency erodes trust in the numbers.

**AI support:** Structure and narrate. Help organize inputs into consistent reporting formats and draft the plain-English narrative around figures a person has verified.

**Skills that serve this layer:** [Principal Weekly Brief](../skills/principal-weekly-brief/) (the reporting cadence), supported by the [templates](../templates/).

**Human boundary:** AI never originates financial figures and never presents numbers as verified. People own the data; AI helps present it.

## Layer 6 — Deal flow

**Function:** Managing inbound and sourced opportunities through a consistent evaluation pipeline.

**The problem:** Deal flow is uneven and easy to handle inconsistently, so good opportunities get thin reviews and weak ones consume time.

**AI support:** Standardize the front of the funnel. Triage inbound opportunities into a consistent first-pass memo, generate diligence question sets, and flag missing information — so every opportunity gets the same disciplined initial treatment.

**Skills that serve this layer:** [Investment Memo Screener](../skills/investment-memo-screener/), [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/).

**Human boundary:** AI screens for structure and completeness; investment judgment and any decision to pursue, pass, or commit are entirely human.

## Layer 7 — Institutional memory

**Function:** What the office knows and remembers — decisions made, why they were made, who owns what, and what was learned.

**The problem:** In a lean office, memory lives in individuals. When attention is scarce, context is lost between meetings and across years.

**AI support:** Capture and organize. Convert meetings into durable records of decisions, owners, and deadlines; digest documents into retained plain-English notes; and keep the office's working record consistent and searchable.

**Skills that serve this layer:** [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/), [Document Digest](../skills/document-digest/).

**Human boundary:** People decide what belongs in the record and verify it. The memory is only as trustworthy as the human review behind it.

## Layer 8 — Executive decision support

**Function:** Giving the principal and senior operators the concentrated, well-framed context they need to make good decisions quickly.

**The problem:** Decision-makers are time-constrained and need signal, not raw material.

**AI support:** Synthesize across the layers below into decision-ready briefings — the week ahead, the decisions pending, the risks emerging, the meetings that matter — so the principal's time is spent deciding, not assembling.

**Skills that serve this layer:** [Principal Weekly Brief](../skills/principal-weekly-brief/), [Meeting Prep Pack](../skills/meeting-prep-pack/).

**Human boundary:** This is the top of the model precisely because the decisions live here. AI frames the decision; the principal makes it.

## The through-line

Across all eight layers, the pattern is the same:

> **AI absorbs the structure-heavy work. Humans keep the judgment, the relationships, and the risk.**

That division is what makes the model both practical and conservative. It lets a lean team cover a wider surface area with more consistent preparation, without surrendering control of any consequential decision. It is not a claim that AI replaces headcount, judgment, or professional advice.

## Going deeper

This operating model describes the *layers of work*. For the system design that sits around them — context, controls, and measurement — and for how to compose and mature these workflows, see:

- [Reference Architecture](reference-architecture.md) — the six-layer architecture with review gates and feedback.
- [AI Workforce Operating Model](ai-workforce-operating-model.md) — what an AI Workforce is, and what stays human.
- [Skill Maturity Matrix](skill-maturity-matrix.md) — from a one-off prompt to an operating layer.
- [System blueprints](../blueprints/) — composed, end-to-end designs across briefings, deal review, meetings, and vendors.

---

*This operating model is a conceptual and operational framework, not legal, compliance, investment, or regulatory advice. Adapt it to your own structure and obligations.*
