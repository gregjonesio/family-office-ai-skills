# Playbook: Insurance Renewal Management

How a family office manages renewals across a layered personal-risk program — maintaining a renewal calendar and current schedule of values, reading each renewal for changes and gaps, confirming named insureds match entity ownership, and periodically re-marketing — before anything is bound and without rendering insurance advice. Read-only, human-in-the-loop, non-advisory.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, policy, carrier, or broker. Nothing here binds, declines, or recommends coverage, and none of it is insurance, legal, or tax advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Approach every renewal prepared: know what changed from the expiring policy, where coverage may have gaps, whether limits still match values, and whether titling and named insureds still match how assets are owned — so the renewal decision is informed and on time, with no lapse and no detail missed, and the coverage judgment stays with the broker and the family.

## Operating Problem

A UHNW insurance program is not a stack of consumer policies; it is a structured program — primary property layered under excess and umbrella liability towers, valuable-articles floaters for art, jewelry, and collections, coverage for domestic staff (workers' compensation and employment practices), and specialty lines such as aviation, marine, cyber, and kidnap-and-ransom. Each policy renews on its own cycle with dense wording and quiet changes to limits, exclusions, and endorsements. The risks are asymmetric and specific: a **missed renewal date** causes a lapse; an **insurance-to-value gap** leaves a home underinsured as rebuild costs rise or a collection appreciates past its limit; and a **titling mismatch** — an asset held in an LLC or trust that is not a named insured — can void coverage at claim time. A lean office reads each renewal under deadline; the discipline a mature program imposes is a master renewal calendar, a maintained schedule of values with periodic appraisals, and a broker-of-record relationship that is re-marketed every few years rather than left to auto-renew.

## Typical Trigger

A renewal notice or quote arrives from the broker or carrier, or the renewal calendar flags an upcoming expiration with enough lead time to run the pre-renewal process (commonly begun 90–120 days out).

## Frequency

Recurring on each policy's renewal cycle — staggered across the year — with the broader program re-marketed periodically (often every few years) and the schedule of values refreshed on an appraisal cadence.

## Primary Stakeholders

- **COO / operations (owner)** — maintains the renewal calendar and schedule of values, reviews renewals, and prepares the decision.
- **Principal / family** — make the coverage decision and accept the risk.
- **Broker / agent (broker of record)** — advises on coverage, markets the program, advocates on claims, and binds; the office's review supports, not replaces, that advice.
- **Counsel** — consulted on policy language, named insureds, and how coverage maps to entity and trust ownership.

## Required Inputs

- The renewal notice or quote and the proposed policy
- The expiring policy for line-by-line comparison
- The schedule of values, recent appraisals, and the asset/entity ownership map
- Endorsements, scheduled items, and loss runs (claims history)
- Known changes since last renewal — new homes, vehicles, art, watercraft, staff, or entities

Policy documents, schedules, and asset detail are highly sensitive; provide them manually after review.

## AI-Assisted Activities

- Produce a plain-English read of the renewal and policy with [Document Digest](../skills/document-digest/): key dates, limits, exclusions, endorsements, obligations, unusual terms flagged, and precise questions for the broker or counsel — **without giving insurance advice**.
- Structure a renewal review with [Vendor Review](../skills/vendor-review/): terms, changes from the expiring policy, premium considerations, and questions, with a recommended process next step (not a coverage recommendation).
- Prepare for the broker call with [Meeting Prep Pack](../skills/meeting-prep-pack/) and capture follow-ups with [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

AI summarizes, compares, and surfaces questions. It assesses no coverage adequacy, recommends no policy, and binds nothing.

## Human Responsibilities

- Maintain the renewal calendar and the schedule of values, and keep appraisals current on a cadence.
- Decide on coverage with the broker and family — bind, adjust, re-market, or replace.
- Verify every limit, exclusion, named insured, and date against the actual policy.
- Confirm named insureds and additional insureds match current entity and trust ownership.
- Judge coverage adequacy and gaps — the review surfaces questions; the broker advises; the family accepts the risk.
- Watch and meet every renewal deadline; the system surfaces them but does not act.

## Review Gates

1. **Document gate** — verify the digest against the actual policy; do not act on an unreviewed summary.
2. **Change-comparison gate** — a person confirms the identified changes from the expiring policy — limits, exclusions, endorsements, premium — are accurate and complete.
3. **Titling-and-value gate** — a person confirms named insureds match current ownership and that limits still reflect insured values (insurance-to-value), flagging new or appreciated assets for scheduling.
4. **Decision gate** — the family and broker decide on coverage; the AI assesses no adequacy and makes no recommendation.
5. **Bind-by-deadline gate** — a person confirms the renewal is bound before expiration; no lapse, no gap between policies.

## Outputs

- A plain-English digest of the renewal and policy (draft)
- A renewal review with changes, premium notes, and questions (draft)
- A broker-call prep pack and follow-up list (draft)
- A question list for the broker or counsel, including titling and scheduling items (draft)

## Risks

- **Lapse risk** — a missed deadline causes a coverage gap; the bind-by-deadline gate is mandatory and a person owns it.
- **Unnoticed change** — a quiet exclusion or limit change creates a gap; the change-comparison gate guards against it.
- **Advice boundary** — outputs are summaries and questions, not insurance advice; coverage adequacy is the broker's and family's call.
- **Hallucination** — the AI may misread a limit or term; all are verified against the policy.
- **Confidentiality** — policies expose assets and exposures; use approved environments. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).

## Common Failure Points

- **Titling mismatch.** A home or vehicle is held in an LLC or trust that is not a named insured, so a claim is denied. *Control:* the titling-and-value gate reconciling named insureds against the current ownership map, with counsel on the structure.
- **Underinsurance to value.** Rebuild costs rise or a collection appreciates past its scheduled limit, leaving a shortfall discovered only at loss. *Control:* a maintained schedule of values with periodic appraisals and an insurance-to-value check at renewal.
- **Lapse from a missed date.** A renewal date passes unnoticed and coverage gaps. *Control:* a master renewal calendar with lead-time alerts and the bind-by-deadline gate.
- **Auto-renewal of a stale program.** The same program renews year after year without re-marketing, so the family overpays or carries the wrong coverage. *Control:* periodic re-marketing through the broker of record and a benchmarking review.
- **New assets never scheduled.** A newly acquired home, car, boat, or artwork is never added, so it is uninsured or under a default limit. *Control:* a standing intake that routes acquisitions to the schedule, checked at the titling-and-value gate.
- **No claims-history review.** Loss runs are never examined, so recurring exposures and their pricing impact go unmanaged. *Control:* a loss-run review as part of the pre-renewal process.

## Metrics

- Renewals bound before their deadline (target: 100%, zero lapses)
- Review-gate completion rate (target: 100%)
- Changes from expiring policy identified and confirmed
- Schedule of values and appraisals current within the office's cadence
- Program re-marketed within the office's interval
- Review time saved per renewal (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Document Digest](../skills/document-digest/)
- [Vendor Review](../skills/vendor-review/)
- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Vendor Management System](../blueprints/vendor-management-system.md) — the review-and-renewal pattern this draws on.

## Related Case Studies

- [Insurance Renewal Review](../case-studies/insurance-renewal-review.md)

## Related Governance Documents

- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [AI Governance for Family Offices](../docs/ai-governance-for-family-offices.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Measurement Framework](../docs/measurement-framework.md)
- [Evaluation and Red-Team Guide](../docs/evaluation-guide.md) and the [Document Digest evals](../evals/document-digest-evals.md)

## Evolution Path

1. **Ad hoc** — policies renew independently, read under deadline, with no consolidated view and frequent auto-renewals.
2. **Calendared and scheduled** — a master renewal calendar and a maintained schedule of values with appraisal cadence prevent lapses and insurance-to-value gaps. These controls stand independent of AI.
3. **Structured and re-marketed** — named insureds reconciled to entity ownership, loss runs reviewed, and the program re-marketed through the broker of record on a set interval.
4. **AI-assisted** — Document Digest and Vendor Review make renewals legible and comparable; approved, read-only retrieval of the expiring policy supports the change comparison — a governed data-access change, not new authority.

No stage lets the AI assess coverage adequacy, recommend a policy, or bind. Coverage judgment stays with the broker and family.

---

*This playbook is an illustrative operating pattern, not insurance, legal, or tax advice, and not a live integration. It binds, declines, and recommends no coverage. Every output described is an unverified draft requiring human review.*
