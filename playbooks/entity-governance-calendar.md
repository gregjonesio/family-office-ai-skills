# Playbook: Entity Governance Calendar

How a family office keeps a multi-entity structure in good standing — maintaining an entity register, tracking annual filings and registered-agent obligations, observing corporate and trust formalities, and preparing resolutions for signature under a signature-authority matrix — with AI surfacing what is coming and reading the underlying documents, while counsel and the office own every filing and determination. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, entity, trust, filing, or jurisdiction. Nothing here is legal, tax, or compliance advice, makes no filing, and renders no governance determination. Every AI output described is an unverified draft requiring human review.

---

## Objective

Keep every entity current and the liability structure intact: annual reports and franchise obligations met on time, registered agents active, beneficial-ownership and license obligations tracked, corporate and trust formalities observed, and resolutions prepared for the right signatories — so nothing lapses and the entity veil holds, with counsel and the office owning each filing and determination.

## Operating Problem

A family structure can span many entities — holding companies, investment LLCs and LPs, operating companies, and trusts — across multiple jurisdictions, each with its own filing deadlines, franchise obligations, registered agents, and governance formalities. The dates are unforgiving and scattered, and the failures are expensive and slow to cure: a missed annual report leads to **administrative dissolution** and the loss of the liability shield; a lapsed **registered agent** can mean a service of process goes unanswered and a default judgment follows; and ignored **corporate formalities** — commingled funds, no resolutions, no separate records — invite veil-piercing that defeats the whole point of the structure. Trusts add their own calendar of trustee actions, distributions, beneficiary notices, and fiduciary accountings. The discipline a mature office imposes is a single entity register, a governance calendar with lead-time alerts, a registered-agent relationship, and a document repository (minute books, org chart, signature matrix) that is the system of record.

## Typical Trigger

An upcoming filing or governance date on the calendar, a notice from a registered agent or jurisdiction, an entity change (formation, dissolution, ownership transfer), or a periodic review of the structure's standing.

## Frequency

Continuous tracking with recurring annual and periodic deadlines per entity and jurisdiction; trust formalities on their own cadence; ad hoc on entity changes.

## Primary Stakeholders

- **COO / general counsel liaison (owner)** — maintains the entity register and calendar and coordinates filings.
- **Counsel** — owns legal determinations, filings, formalities, and governance interpretation.
- **Registered agents and corporate-service providers** — handle jurisdiction-level filings and receive service of process; the office tracks and confirms.
- **Trustees** — own trust actions, distributions, and accountings; the office supports the calendar, not the fiduciary decision.
- **Principal / authorized signatories** — execute resolutions and consents per the signature-authority matrix.

## Required Inputs

- The entity register: each entity with jurisdiction, type, formation date, EIN, registered agent, annual obligations, governing documents, signatories, and ownership chart
- Filing calendars and prior filings per entity
- Registered-agent details and notices
- Governing documents, resolutions, consents, and the signature-authority matrix (provided manually)
- Beneficial-ownership, license, and trust-administration obligations as tracked items
- Notices of any entity change

Entity and governing documents are sensitive; provide them manually in approved environments only.

## AI-Assisted Activities

- Produce plain-English reads of governing documents, notices, and resolutions with [Document Digest](../skills/document-digest/): obligations, recurring dates, signatory requirements, and questions for counsel — **without legal interpretation**.
- Turn the calendar's upcoming obligations into an owned, tracked list with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) (used as an obligations-to-action extractor): owners, deadlines, and dependencies per filing or formality.
- Surface upcoming governance dates and their status in the [Principal Weekly Brief](../skills/principal-weekly-brief/) so nothing approaches unseen.

AI reads, organizes, and reminds. It makes no filing, drafts no resolution as final, interprets no governing document, and renders no governance or legal determination.

## Human Responsibilities

- Maintain the entity register and governance calendar as the system of record.
- Make every filing through counsel or the registered agent, and confirm it was accepted.
- Verify each deadline and requirement against the jurisdiction and governing documents — never rely on a remembered or AI-restated date.
- Observe corporate and trust formalities — separate accounts, resolutions, accountings, beneficiary notices — with counsel and trustees.
- Execute resolutions and consents through the authorized signatories on the matrix.

## Review Gates

1. **Register-accuracy gate** — a person verifies upcoming dates and requirements against the jurisdiction and governing documents; nothing is trusted from memory or the AI alone.
2. **Document gate** — verify any digest against the source governing document before acting; legal questions route to counsel.
3. **Signature-authority gate** — resolutions and consents are executed only by the signatories the matrix authorizes for that entity and action.
4. **Filing-confirmation gate** — counsel or the registered agent makes the filing and the office confirms acceptance; a submitted-but-rejected filing is treated as not filed. The AI never files.

## Outputs

- A current entity governance calendar with upcoming dates and status (draft)
- Plain-English digests of governing documents and notices (draft)
- An owned, tracked obligations list per entity (draft)
- A question list for counsel (draft)

## Risks

- **Lapse risk** — a missed filing can cause penalties or administrative dissolution; the register-accuracy and filing-confirmation gates are mandatory.
- **Stale or wrong date** — jurisdictions and obligations change; every date is verified against source.
- **Drift into legal conclusions** — the digest surfaces questions, not interpretations; governance and legal determinations stay with counsel.
- **Hallucination** — the AI may misread a date or requirement; all are verified against source.
- **Confidentiality** — entity and ownership detail is highly sensitive; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **Administrative dissolution.** A missed annual report or franchise obligation dissolves the entity and removes the liability shield, with cost and delay to reinstate. *Control:* a governance calendar with lead-time alerts and the filing-confirmation gate.
- **Registered-agent lapse.** The agent relationship lapses or an address goes stale, so a service of process is missed and a default judgment follows. *Control:* registered-agent status as a tracked annual item with confirmation.
- **Veil-piercing exposure.** Commingled funds, skipped resolutions, and absent records blur the entity, defeating the structure in litigation. *Control:* observed formalities — separate accounts, documented resolutions, a maintained minute book.
- **Missed beneficial-ownership or license obligation.** A newer or jurisdiction-specific filing obligation is overlooked. *Control:* such obligations tracked as register items and confirmed with counsel, not assumed.
- **Trust formalities skipped.** Required beneficiary notices or fiduciary accountings are missed, creating tax or fiduciary exposure. *Control:* trust actions on the calendar, owned by the trustee with the office tracking dates.
- **Calendar in one person's head.** The structure's obligations live with one staffer and lapse when they are out. *Control:* a central entity register and document repository as the system of record.

## Metrics

- Filings made and confirmed by their deadline (target: 100%, zero lapses)
- Register-accuracy and filing-confirmation gate completion (target: 100%)
- Registered-agent status current across all entities
- Upcoming obligations surfaced with adequate lead time
- Trust and corporate formalities completed on schedule
- Tracking and document-reading time saved (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Document Digest](../skills/document-digest/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)
- [Principal Weekly Brief](../skills/principal-weekly-brief/)

## Related Blueprints

This playbook composes skills directly rather than through a single blueprint. For the layered design it sits within, see the [Reference Architecture](../docs/reference-architecture.md).

## Related Case Studies

- [Meeting-to-Execution Workflow](../case-studies/meeting-to-execution.md) — turning governance discussions into tracked follow-through.

## Related Governance Documents

- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Threat Model](../docs/threat-model.md)
- [Operating Model](../docs/operating-model.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — obligations are remembered informally and tracked in scattered spreadsheets, with lapses cured reactively.
2. **Registered** — a single entity register and a governance calendar with lead-time alerts, backed by a registered-agent relationship, prevent missed filings and lost service of process. These controls stand independent of AI.
3. **Formalized** — observed corporate and trust formalities, a signature-authority matrix, and a document repository (minute books, org chart) as the system of record protect the structure itself.
4. **AI-assisted** — Document Digest makes governing documents legible and the action extractor tracks obligations; approved, read-only retrieval of prior filings can confirm recurring dates — a governed data-access change, not new authority.

No stage lets the AI make a filing, interpret a governing document, or render a governance determination. Those stay with the office and counsel.

---

*This playbook is an illustrative operating pattern, not legal, tax, or compliance advice, and not a live integration. It makes no filing and renders no governance determination. Every output described is an unverified draft requiring human review; legal questions go to counsel.*
