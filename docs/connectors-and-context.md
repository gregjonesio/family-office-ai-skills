# Connectors and Context Access for Family Office AI Workflows

The skills in this repository are the **workflow layer** — they define the work to be done. Connectors are a separate, optional **context-access layer** — they determine how information reaches the workflow. This document explains how connectors fit, what they improve, and the confidentiality, permissioning, governance, and review risk they add.

Connectors can make workflows more useful by reducing manual copy/paste and allowing approved context retrieval. They also enlarge the risk surface. Treat them as a data-access decision to be governed, not a convenience to be switched on.

---

## Purpose

Many AI workflows become more useful when the AI system can access approved context — for example, a calendar, a document repository, email, a task manager, a notes or knowledge base, or a CRM/relationship system — instead of relying entirely on what a person pastes in.

That usefulness is real, but it is conditional. Before adopting connectors, hold these points firmly:

- **Connectors are optional.** They are one way to provide context, not the only way.
- **Connectors are not required to use this repository.** Every skill works with manual input.
- **Connectors are not security controls.** Granting access does not make the workflow safe; it widens what the workflow — and the AI behind it — can reach.
- **Connectors should be scoped, approved, and reviewed** before use, and revisited over time.
- **Manual input is often best for early pilots.** Start by pasting fictional or approved, non-confidential input; add connectors only once a workflow has earned trust.

Adding a connector does not change the repository's posture: the skills remain read-only, human-in-the-loop, and non-advisory. A connector that retrieves context does not authorize the AI to act.

## Operating model

A simple way to picture where connectors sit:

```
Approved data sources → Connectors / context access → AI skill / workflow → Human review → Final output / action
```

- **Skills define the work to be done.** They are the workflow contracts in this repository.
- **Connectors provide context.** They move approved information into the workflow so a person does not have to paste it by hand.
- **Human review remains the control.** Context entering automatically does not reduce the need to verify the output; if anything, it raises it, because the person did not hand-select every input.
- **Final actions remain outside the skill** unless explicitly reviewed and approved by a human. Retrieval is not action. Nothing here sends, writes, approves, or transacts on its own.

## Connector maturity levels

A staged way to think about how much access a workflow has. Higher is not better — higher means more risk and more governance required.

### Level 0 — Manual input only

**Description.** The user manually provides fictional, sanitized, or approved non-confidential input.

**Use for.** Pilots, testing, public AI tools, and high-risk documents.

**Risk.** Lowest, but manual and incomplete — a person curates every input, which is slow but the lowest-risk option.

### Level 1 — Read-only approved connectors

**Description.** The AI can retrieve from approved systems but cannot write, send, delete, approve, or transact.

**Use for.** Meeting prep, document retrieval, brief drafts, task summaries.

**Risk.** Context exposure and permission scope — the connector can reach more than any single task needs.

### Level 2 — Read-only connectors plus draft creation

**Description.** The AI can retrieve context and produce drafts for human review.

**Use for.** Draft emails, draft meeting briefs, draft memos, draft action lists.

**Risk.** False confidence, stale context, and accidental inclusion of sensitive information pulled in automatically.

### Level 3 — Write-capable connectors

**Description.** The AI can create or modify records, tasks, documents, or messages.

**Use for.** Not recommended generally. This requires formal approval, access controls, logging, and human review before any adoption. It is beyond what these templates assume.

**Risk.** Unauthorized changes, recordkeeping issues, confidentiality leakage, and operational errors.

### Level 4 — Autonomous action workflows

**Description.** The AI can act without human approval.

**Use for.** Out of scope for this repository.

**Risk.** Not appropriate for these public templates. The repository's posture is human-in-the-loop; autonomous action is the line it does not cross.

## Common connector categories

Generic categories only — no specific private systems are named. Recommended posture is, in nearly every case: manual or read-only first, least privilege, no autonomous sending or changes, and human review required.

| Connector category | Example sources (generic) | Useful for | Key risks | Recommended posture |
|--------------------|---------------------------|------------|-----------|---------------------|
| Calendar | A calendar application | Meeting prep, weekly briefs | Exposure of attendees, travel, locations | Read-only first; least privilege; human review |
| Email | A mailbox | Follow-ups, context for briefs | Broad exposure of sensitive correspondence | Manual or narrow read-only; no autonomous send; human review |
| Document repository | A cloud drive or document store | Document digests, diligence context | Accidental retrieval of confidential or privileged files | Read-only; scoped folders; human review |
| Task / project management | A task or project tracker | Action lists, status summaries | Stale or incomplete task data | Read-only first; least privilege; human review |
| CRM / relationship system | A contact/relationship tool | Meeting prep, relationship context | Exposure of private relationship notes | Read-only; scoped; human review |
| Notes / knowledge base | A notes or knowledge app | Institutional memory, prior context | Inclusion of sensitive internal notes | Read-only; scoped; human review |
| Accounting / reporting exports | Exported reports or summaries | Reporting context (figures verified by a person) | Financial-data sensitivity; staleness | Manual export or read-only; human verification of all figures |
| Investment research / data rooms | A diligence data room or research store | Manager and deal context | Confidential investment material; access scope | Read-only; explicit approval; human review |

## Connector approval checklist

Work through this before connecting anything. If you cannot answer an item, you are not ready to connect that system.

- [ ] What system is being connected?
- [ ] What data types are included?
- [ ] Is confidential, personal, financial, legal, tax, health, or account information present?
- [ ] Who approved the connector?
- [ ] Is access read-only?
- [ ] What exactly can the AI retrieve?
- [ ] Can the AI write, send, delete, or modify anything?
- [ ] Are permissions scoped to the minimum necessary (least privilege)?
- [ ] Are logs available?
- [ ] Can access be revoked quickly?
- [ ] Is there a human-review step before any output is used?
- [ ] Does this create recordkeeping obligations?
- [ ] Is the AI tool approved for this data type and its data-handling terms acceptable?
- [ ] Has counsel or compliance reviewed it, where applicable?

## Skill-by-skill connector examples

Illustrative context sources for the current skills. In every case the posture is the same: **manual or read-only first, no autonomous write/send, human review required.** These describe *possible* context sources, not connectors included in this repository.

| Skill | Useful context sources (generic) | Connector posture | Notes |
|-------|----------------------------------|-------------------|-------|
| Principal Weekly Brief | Calendar, task list, prior weekly notes, approved project tracker | Manual or read-only first; no autonomous write/send; human review required | Calendar/travel data is sensitive; scope tightly |
| Investment Memo Screener | Approved deal notes, pitch materials, diligence tracker | Manual or read-only first; no autonomous write/send; human review required | Deal material is confidential; confirm the tool is approved for it |
| Manager Diligence Summarizer | Manager deck, DDQ, approved performance summaries | Manual or read-only first; no autonomous write/send; human review required | Treat all retrieved figures as unverified |
| Meeting Prep Pack | Calendar event, prior notes, agenda, contact notes | Manual or read-only first; no autonomous write/send; human review required | Relationship/contact notes can be highly sensitive |
| Post-Meeting Action Extractor | Meeting transcript/notes, task system | Manual or read-only first; no autonomous write/send; human review required | The follow-up draft is internal; a person reviews and sends |
| Vendor Review | Proposal, renewal notice, service notes, contract summary | Manual or read-only first; no autonomous write/send; human review required | Route contract terms to counsel; do not act on retrieval |
| Document Digest | Approved document repository or manually uploaded document | Manual or read-only first; no autonomous write/send; human review required | High-risk documents are best provided manually after review |

## What not to connect

The following data categories are prohibited or high-risk for these public templates. This is not a claim that they can never be used under any circumstances — it is that they require **explicit approval, appropriate systems, and professional review**, and are **outside the scope of this public repository**.

- Personal identity documents
- Account numbers
- Login credentials
- API keys
- Health information
- Unredacted tax returns
- Estate planning documents — unless approved and reviewed
- Confidential investment documents — unless the AI system is approved for that data
- Attorney-client privileged material — unless counsel approves
- Employment or HR records
- Private family information
- Live trading or banking systems
- Systems that allow transaction approval, wire approval, or communication sending

If a workflow seems to require one of these, stop and route the decision to the people accountable for the office's confidentiality, security, and compliance.

## Practical implementation sequence

1. **Start with manual input.** Paste fictional or approved, non-confidential material.
2. **Pilot one read-only source.** Choose a single, low-sensitivity system.
3. **Limit scope to one workflow.** Do not connect a source to everything at once.
4. **Test with fictional or approved data.** Confirm behavior before any real context flows.
5. **Review outputs manually.** Verify facts; check for sensitive material pulled in automatically.
6. **Track errors and omissions.** Note stale context, over-broad retrieval, and mistakes.
7. **Expand only after governance review.** Add sources or scope deliberately, not opportunistically.
8. **Avoid write/actions until formal controls exist.** No write-capable or autonomous connectors without approval, access controls, logging, and human review.

## Key principle

> **Connectors improve context. They do not replace judgment, permissioning, review, or professional responsibility.**

---

*This document is practical operational guidance, not legal, compliance, cybersecurity, or professional advice. It describes how to think about connectors; it does not provide, recommend, or include any live integration. Adapt it to your structure and obligations with qualified advisers.*
