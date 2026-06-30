# Playbook: Principal Weekly Review

How a family office turns a week of scattered inputs — calendar, open decisions, investment updates, operational issues, travel, and pending follow-ups — into one consistent briefing the principal can read and act on. Read-only, human-in-the-loop, non-advisory: AI drafts the brief; a person owns what it says.

> **Fictionalized and illustrative.** This is a generalized operating pattern. It does not describe any actual family office, principal, investment, or operating environment. Nothing here is investment, legal, tax, accounting, compliance, or fiduciary advice. Every AI output described is an unverified draft requiring human review.

---

## Objective

Produce a single, consistently formatted weekly briefing that gives the principal an accurate picture of what needs attention — decisions pending, items in motion, and what is coming — so scarce executive attention is spent on judgment, not on assembling the picture. A well-run brief is a *decision-forcing document*: every open item carries an owner, a staff recommendation, and a "needed-by" date, so the meeting drives closure rather than status.

## Operating Problem

The week's signal arrives in fragments: emails, calls, calendar invites, deal updates, operational exceptions, and the principal's own verbal asks. A lean office reassembles this by hand every week, under time pressure, and the result varies with whoever wrote it. The deeper problem is that most offices lack a single source of truth — items live in one person's inbox and head — so the brief either bloats into an unread status report or quietly drops the things that matter. The discipline a mature office imposes is that the brief is a *read-out of a maintained tracker*, not a parallel document rebuilt from memory each week.

## Typical Trigger

A standing weekly cadence — the brief lands at a fixed time (commonly Sunday evening or first thing Monday) ahead of the principal's week — plus a "no surprises" rule that escalates urgent items immediately rather than holding them for the cycle.

## Frequency

Weekly, with a fixed production window and a staff input cutoff. Many offices add a lighter mid-week touch and a standing weekly principal/chief-of-staff sync to work the brief live.

## Primary Stakeholders

- **Chief of staff (owner)** — the single point of accountability ("one throat to choke") for what reaches the principal; maintains the master tracker and runs the production cadence.
- **Principal** — the reader and decision-maker; the brief exists to protect their attention.
- **Investment, operations, finance, and EA staff** — contributors who submit updates and open items by the cutoff.
- **Spouse / family members** — recipients of a tailored view where the office serves the broader family, with discretion tiers governing what each sees.

## Required Inputs

- Calendar items and meetings for the coming week (office and, where appropriate, personal/family)
- Open decisions awaiting the principal, each with a recommendation and a needed-by date
- Investment and portfolio updates (as provided, treated as unverified)
- Operational issues, exceptions, and approvals pending
- Travel notes and logistics
- Pending follow-ups carried from prior weeks
- A "parking lot" of items not yet ripe for decision

Provide sanitized or approved, non-confidential material only. Keep account numbers and identifiers out unless the task requires them.

## AI-Assisted Activities

- Consolidate the week's submitted inputs into the office's standard brief format using the [Principal Weekly Brief](../skills/principal-weekly-brief/) skill.
- Carry forward unresolved follow-ups from the prior brief so nothing silently drops between cycles.
- Surface dates, deadlines, and decisions that need the principal's attention, and flag any open item missing an owner or a needed-by date.
- Where the week includes a notable meeting, draft prep with [Meeting Prep Pack](../skills/meeting-prep-pack/); where it follows one, fold in the owned items from [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/).

AI consolidates, formats, and reminds. It makes no recommendation and renders no judgment on any investment or operational item.

## Human Responsibilities

- Maintain the master tracker as the single source of truth; the brief reads out of it.
- Verify every figure, date, and claim against source before it reaches the principal.
- Decide what belongs in the brief and what is noise, and apply discretion tiers — what is for the principal only, for the spouse, or for the broader family.
- Own the framing of every open decision (owner, recommendation, needed-by); the brief presents decisions, it does not resolve them.
- Capture the principal's verbal asks back into the tracker so they are not lost.

## Review Gates

1. **Inputs gate (staff cutoff)** — contributors submit by a fixed deadline; the owner confirms inputs are appropriate to process and free of unapproved confidential data. A cutoff is itself a control: it prevents a brief assembled from whatever happened to land last.
2. **Accuracy gate (verification against source)** — a competent person verifies figures, dates, and names against the current record; nothing remembered is trusted over source.
3. **Editorial and discretion gate (single owner)** — the chief of staff confirms the brief is complete, correctly prioritized, makes no recommendation the office did not intend, and respects the discretion tier for each recipient before release.

## Outputs

- A consolidated weekly principal brief (draft)
- A carried-forward follow-up and decision log (draft)
- Meeting prep for the week's key meetings, where relevant (draft)

## Risks

- **Stale information** — a remembered number or date can be wrong; every item is verified against the current record.
- **Hallucination** — the AI may invent or misstate an item; the accuracy gate catches it.
- **Overreliance** — a polished brief can create false confidence; it remains a draft until reviewed.
- **Confidentiality** — briefs aggregate sensitive context across the family; use only approved environments and respect discretion tiers. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Advice boundary** — the brief organizes items for decision; it gives no investment or other professional advice.

## Common Failure Points

- **No single source of truth.** When items live in one person's inbox, the brief is rebuilt from memory each week and quality swings with the author's recall. *Control:* a maintained master tracker that the brief reads out of, not a fresh document each cycle.
- **Key-person dependency.** Only the chief of staff can produce the brief, with no documented template or tracker — the cadence breaks the week they are out. *Control:* a documented format and a shared tracker so a backup can run it.
- **Status report, not decision document.** The brief grows into pages of updates with no decisions framed, and the principal stops reading it. *Control:* every open item carries an owner, a recommendation, and a needed-by date; updates live in an appendix.
- **Decisions surfaced without a recommendation or deadline.** Items raised as open questions with no staff point of view drift week to week. *Control:* staff must take a position before an item reaches the principal.
- **Verbal asks lost.** The principal asks for something in passing and it never enters the system. *Control:* a standing habit of logging verbal asks straight into the tracker, reviewed at the weekly sync.
- **Discretion failure.** A sensitive family item reaches the wrong recipient because the brief had one undifferentiated distribution. *Control:* explicit discretion tiers governing who sees what.

## Metrics

- Brief delivered on time against the standing cadence (target: every week)
- Review-gate completion rate (target: 100%)
- Open decisions closed within their needed-by date vs. carried over
- Follow-ups carried to closure vs. dropped
- Time saved in assembly (directional)

Figures are directional, not audited. See [measurement-framework.md](../docs/measurement-framework.md).

## Related Skills

- [Principal Weekly Brief](../skills/principal-weekly-brief/)
- [Meeting Prep Pack](../skills/meeting-prep-pack/)
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)

## Related Blueprints

- [Weekly Principal Briefing System](../blueprints/weekly-principal-briefing-system.md)

## Related Case Studies

- [Weekly Principal Brief](../case-studies/weekly-principal-brief.md)

## Related Governance Documents

- [Operating Model](../docs/operating-model.md)
- [Privacy and Confidentiality](../docs/privacy-and-confidentiality.md)
- [Connectors and Context Access](../docs/connectors-and-context.md)
- [Measurement Framework](../docs/measurement-framework.md)

## Evolution Path

1. **Ad hoc** — the brief is rebuilt from inboxes each week; quality depends on who writes it and key-person risk is high.
2. **Templated** — a documented format and a standing input cutoff make the brief consistent and reduce dependence on any one author.
3. **Single source of truth** — a maintained decision-and-action tracker becomes the system of record; the brief reads out of it, and open items carry owners, recommendations, and needed-by dates.
4. **AI-assisted** — the [Principal Weekly Brief](../skills/principal-weekly-brief/) skill drafts the read-out from the tracker, and approved, read-only retrieval of calendar and prior follow-ups reduces copy-and-paste — treated as a governed data-access change, not new authority. See [connectors-and-context.md](../docs/connectors-and-context.md).

The accuracy, editorial, and discretion gates stay human at every stage. The brief never becomes a decision or a recommendation.

---

*This playbook is an illustrative operating pattern, not legal, compliance, investment, tax, or fiduciary advice, and not a live integration. It does not approve, transact, or send anything. Every output described is an unverified draft requiring human review.*
