# AI-Native Family Office Reference Architecture

How the skills in this repository fit into a broader AI-native family office operating model. This is a system design reference, not a product and not a deployment. It describes layers and controls — not software to install. Everything remains read-only, human-in-the-loop, model-agnostic, and non-advisory.

The central idea: an AI-native family office is not "a chatbot plus prompts." It is a layered operating model where each layer has a purpose, a risk profile, and a control. The skills are one layer; they only work well when the layers around them — context, governance, review, and measurement — are in place.

---

## The architecture at a glance

```
Approved Sources
  → Context Access / Connectors
  → Workflow Skills
  → Human Review Gates
  → Operator / Principal Outputs
  → Measurement + Feedback
        (feeds back into sources, skills, and governance)
```

Read it as a pipeline with a control gate in the middle:

- **Skills define the work.** They turn inputs into structured drafts.
- **Connectors provide approved context.** They move information into the workflow; they are optional and are a data-access risk, not a control.
- **Human review gates are the controls.** Nothing consequential passes without a competent person.
- **Outputs remain drafts until reviewed.** A draft is not a decision, a communication, or an action.
- **Measurement improves the system over time.** Feedback tunes inputs, skills, and governance.

## Layer 1 — Data / Context Layer

**Purpose.** The information the office works from: calendars, documents, notes, task systems, correspondence, reporting exports, research.

**Examples.** A weekly calendar feeding a brief; a document provided for a digest; meeting notes feeding an action register. (Generic categories only — no specific systems.)

**Risks.** Confidentiality exposure; sensitive data handled in unapproved tools; stale or incomplete information; aggregation of individually harmless details into sensitive ones.

**Review / control requirements.** Use an approved environment with acceptable data terms; minimize and de-identify; never paste highly sensitive material into public tools. See [privacy-and-confidentiality.md](privacy-and-confidentiality.md).

## Layer 2 — Connector Governance Layer

**Purpose.** Govern how (and whether) context is retrieved automatically rather than pasted by hand. This layer decides what may be connected, at what scope, and under what approval.

**Examples.** A read-only, scoped connection to an approved calendar for meeting prep; a manual export instead of a live connection for sensitive reporting.

**Risks.** Overly broad permissions; accidental retrieval of privileged or confidential material; write- or send-capable access; access not revoked after a role change.

**Review / control requirements.** Least privilege; read-only first; approved systems only; a connector inventory; logging; a revocation process; explicit approval. Connectors are not security controls. See [connectors-and-context.md](connectors-and-context.md).

## Layer 3 — Workflow Skills Layer

**Purpose.** The repeatable workflows themselves — the `SKILL.md` contracts that turn inputs into structured drafts (briefs, memos, digests, action lists).

**Examples.** [Principal Weekly Brief](../skills/principal-weekly-brief/), [Investment Memo Screener](../skills/investment-memo-screener/), [Document Digest](../skills/document-digest/), and the rest of the [skills](../skills/).

**Risks.** Hallucination; presenting assumptions as fact; advice creep; following injected instructions in source material; over-trust from clean formatting.

**Review / control requirements.** Each skill's `Quality control` and `Do not` sections; separation of facts from assumptions; flagging of missing information. These are instructions to the model, not enforceable controls — the control is the next layer.

## Layer 4 — Review / Control Layer

**Purpose.** The human gates between a draft and any use of it. This is the primary control in the entire architecture.

**Examples.** A reviewer verifying a brief's facts before it reaches a principal; counsel reviewing a document the digest flagged; an investment committee handling anything the screener surfaced.

**Risks.** Skipped review under time pressure; rubber-stamping; "the AI generated it" used as an excuse for an unverified error.

**Review / control requirements.** Review scaled to consequence (spot-check → verify facts → named reviewer → human writes/sends). The reviewer is accountable for the output as if they produced it. See the human-review model in [threat-model.md](threat-model.md).

## Layer 5 — Principal / Operator Output Layer

**Purpose.** The reviewed artifacts that reach a principal or operator and support a decision: the brief, the memo, the action register, the digest.

**Examples.** A verified weekly brief; a screened first-pass memo routed to committee; a clean action list with owners and deadlines.

**Risks.** Outputs treated as decisions rather than inputs to a decision; outputs forwarded through channels not appropriate for the underlying data.

**Review / control requirements.** Outputs are decision-*support*, never decision-*making*. Final actions — sending, approving, allocating, transacting — remain human and outside the skill. Store outputs under the same controls as their sources.

## Layer 6 — Measurement / Feedback Layer

**Purpose.** Observing whether the system helps, and feeding that back into the other layers. Honest, directional measurement — not audited metrics.

**Examples.** Tracking workflows executed, human-review completion, correction rate, and confidentiality incidents; noting recurring corrections that indicate a skill or input needs tuning.

**Risks.** Overstated value claims; metrics that flatter; measuring activity while ignoring governance.

**Review / control requirements.** Prioritize governance metrics (review completion, confidentiality incidents). Keep value figures internal, directional, and caveated. See [measurement-framework.md](measurement-framework.md).

## How the layers work together

- A workflow is only as trustworthy as **Layer 4** behind it. Strong skills with weak review is an unmanaged risk.
- **Layer 2** is optional. Many offices run the whole architecture on manual input (Layer 1 → Layer 3) for a long time, and that is a legitimate, lower-risk choice.
- **Layer 6** is what turns a collection of skills into an improving system rather than a static prompt library.
- No layer grants autonomy. Adding capability raises the importance of the control and governance layers, never lowers it.

---

*This reference architecture is a conceptual and operational framework, not legal, compliance, investment, cybersecurity, or regulatory advice, and not a deployment or product. It describes controls and layers; it does not provide or include any live integration. Adapt it to your structure and obligations with qualified advisers.*
