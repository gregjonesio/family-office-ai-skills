# Playbook: Vendor Onboarding & Review

How a family office onboards new service providers and periodically reviews existing ones — running due diligence, collecting insurance and tax documentation, controlling access, separating who approves a vendor from who pays it, and offboarding cleanly — without approving, signing, terminating, or sending anything. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, vendor, contract, or service provider. Nothing here approves, signs, renews, or terminates an agreement, and none of it is legal, procurement, or tax advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Bring on and maintain service providers through a consistent, controlled process: agreements read into plain English, due diligence and documentation collected before access is granted, terms and risks surfaced, periodic reviews run on a cadence, and access revoked cleanly at offboarding — so the vendor roster stays current, insured, and benchmarked, with a person owning every decision and no single individual able to both engage a vendor and pay it.

## Operating Problem

A family office relies on many providers across very different risk profiles — custodians and banks, technology and data vendors, accounting and legal firms, and household and personal-access vendors who hold keys, codes, and proximity to the family. Onboarding means reading an unfamiliar agreement under time pressure and deciding what diligence the vendor's access warrants; periodic review means catching service issues, fee creep, lapsed insurance, and auto-renewals before they compound. Two structural weaknesses recur in lean offices: **no segregation of duties**, so the person who selects and approves a vendor also approves and pays its invoices — the textbook fraud and error exposure; and **no offboarding discipline**, so a former vendor keeps a key, a login, or system access long after the relationship ends. The discipline a mature office imposes is a documented onboarding checklist tiered to access risk, an approved-vendor list with competitive-bid thresholds, separation of approval from payment, and a periodic access review.

## Typical Trigger

A new vendor is selected and needs onboarding, a renewal or proposal arrives, a service issue is raised, or the periodic review cadence comes due for an existing provider.

## Frequency

On onboarding and on each renewal, plus a periodic (often annual) review of active providers and an access review; service issues arise as needed.

## Primary Stakeholders

- **Operations lead (owner)** — runs onboarding and reviews, collects documentation, and prepares the decision.
- **Approver / principal** — decides whether to engage, renew, renegotiate, or replace, within authority limits.
- **Accounts-payable function** — pays approved invoices; under segregation of duties, the approver of a vendor is not the person who releases its payments.
- **Counsel** — handles contractual questions; the digest's questions route to them, not around them.
- **The vendor** — the counterparty; the office communicates directly.

## Required Inputs

- The vendor proposal, renewal notice, or invoice
- The contract or contract excerpt, including any auto-renewal/evergreen and notice provisions
- Onboarding documentation appropriate to the vendor's risk tier: references, background checks for household/personal-access vendors, certificate of insurance (COI), W-9, confidentiality/NDA, and a SOC 2 or equivalent for technology and data vendors
- Service notes and performance history
- The approved-vendor list and the office's onboarding and approval policy, including bid thresholds

Contracts and diligence materials are sensitive; provide high-risk documents manually after review.

## AI-Assisted Activities

- Produce a plain-English read of the proposal, renewal, or contract with [Document Digest](../skills/document-digest/): key dates, obligations, unusual terms, and auto-renewal and notice provisions flagged, with questions for counsel.
- Structure a review with [Vendor Review](../skills/vendor-review/): terms, service issues, cost considerations, documentation status, risks, vendor questions, and a recommended process next step.
- Prepare for the vendor or negotiation conversation with [Meeting Prep Pack](../skills/meeting-prep-pack/).
- Capture follow-ups, documentation gaps, and escalations after the conversation with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

AI reads, structures, and surfaces questions. It assesses no pricing fairness, draws no legal conclusion, approves nothing, and sends nothing.

## Human Responsibilities

- Decide whether to engage, renew, renegotiate, escalate, or replace, within authority limits.
- Run diligence proportionate to the vendor's access — heavier for household and data vendors.
- Collect and keep current the COI, W-9, and NDA before access or payment is granted.
- Verify terms and figures against the actual agreement, and route contractual questions to counsel.
- Keep vendor approval separate from invoice payment, and own all communication and any signature.
- Run the periodic access review and execute clean offboarding when a relationship ends.

## Review Gates

1. **Onboarding-diligence gate** — before a vendor is active, a person confirms the risk-tiered diligence is complete: references and background checks where access warrants, a current COI, a W-9, and an NDA on file.
2. **Document gate** — verify the digest against the source agreement; do not act on an unreviewed summary.
3. **Review gate** — confirm the vendor review's terms and figures, and confirm it makes no fairness or legal determination.
4. **Approval-vs-payment gate (segregation of duties)** — the person who approves the engagement is not the person who releases its payments; competitive-bid thresholds are met for spend above the policy limit.
5. **Notice-and-offboarding gate** — a person tracks auto-renewal and notice deadlines so none passes unintentionally, and on termination confirms access (keys, codes, logins, system permissions) is revoked and property returned.

## Outputs

- A plain-English digest of the agreement (draft)
- A vendor review memo with terms, risks, and documentation status (draft)
- Negotiation or relationship-review prep (draft)
- An action and escalation list, including documentation and access items (draft)

## Risks

- **Unintentional auto-renewal** — a missed notice deadline locks in a renewal; the notice-and-offboarding gate guards against it.
- **Reliance on an unreviewed summary** — a digest is not the contract; the document gate is mandatory.
- **Drift into legal or procurement conclusions** — the review asserts no fairness and no legal interpretation; contractual questions go to counsel.
- **Hallucination** — the AI may misread a term or figure; all are verified against source.
- **Confidentiality** — contracts and diligence expose terms and counterparties; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **No segregation of duties.** One person selects the vendor, approves its invoices, and releases payment — the classic fraud and error exposure. *Control:* approval separated from payment, enforced in the AP workflow.
- **Evergreen auto-renewal.** A self-renewing contract locks in a poor or overpriced vendor because the notice window passed. *Control:* notice and renewal dates tracked on a vendor register with lead-time alerts.
- **Lapsed insurance.** A vendor's COI expires and an uninsured contractor is working on the property when something goes wrong. *Control:* COI expiry tracked and refreshed as a condition of continued engagement.
- **Access not revoked at offboarding.** A former vendor retains keys, alarm codes, or system logins. *Control:* an offboarding checklist that revokes access and recovers property, confirmed at the offboarding gate.
- **Skipped background check on a personal-access vendor.** A household vendor with proximity to the family is engaged without screening. *Control:* risk-tiered diligence requiring background checks for personal-access roles.
- **Fee creep with no benchmarking.** Pricing drifts upward across renewals because the service is never re-bid. *Control:* competitive-bid thresholds and periodic benchmarking.

## Metrics

- Vendors reviewed before renewal deadlines (target: 100%)
- Unintentional auto-renewals (target: zero)
- Onboarding diligence complete before access granted (target: 100%)
- COIs current across active vendors
- Access revoked at offboarding (target: 100%, no lingering access)
- Review-gate completion rate (target: 100%)
- Review time saved per vendor (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Vendor Review](../skills/vendor-review/)
- [Document Digest](../skills/document-digest/)
- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Vendor Management System](../blueprints/vendor-management-system.md)

## Related Case Studies

- [Insurance Renewal Review](../case-studies/insurance-renewal-review.md) — a vendor-renewal review in practice.

## Related Governance Documents

- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Threat Model](../docs/threat-model.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — vendors engaged informally, documentation collected inconsistently, and one person handling selection, approval, and payment.
2. **Controlled** — a documented onboarding checklist tiered to access risk, an approved-vendor list, competitive-bid thresholds, and segregation of approval from payment. These controls stand independent of AI.
3. **Registered** — a vendor register tracking COI and renewal dates, periodic access reviews, and a standing offboarding checklist close the lifecycle.
4. **AI-assisted** — Document Digest and Vendor Review make agreements legible and reviews consistent; approved, read-only retrieval of the active contract supports periodic review — a governed data-access change, not new authority.

No stage lets the AI approve, sign, renew, or terminate an agreement, or assess pricing fairness. Those stay human, with counsel on contractual questions.

---

*This playbook is an illustrative operating pattern, not legal, procurement, or tax advice, and not a live integration. It approves, signs, renews, and terminates nothing. Every output described is an unverified draft requiring human review; route contractual questions to counsel.*
