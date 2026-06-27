# Case Study: Weekly Principal Brief

How a lean family office turns a week of scattered inputs into one consistent principal briefing — drafted by AI, verified by a person, delivered by a person.

> **Fictionalized and illustrative.** This is a sanitized, generalized example. It does not describe any actual family office, employer, client, principal, vendor, or operating environment. All names, scenarios, and figures are invented and directional. Nothing here is investment, legal, tax, accounting, compliance, or fiduciary advice.

---

## Scenario

A single operator supports a principal who wants a short Monday-morning read on the week ahead: what is on the calendar, what decisions are waiting, what moved on investments and operations, which vendor issues are open, and what is still owed from last week. The raw material is spread across a calendar, a task list, last week's meeting notes, and a handful of email threads. The principal does not want a data dump — they want a tight, consistent brief they can read in a few minutes.

## Operating problem

A lean office has no dedicated chief of staff with hours to assemble this by hand every week. The inputs are scattered, the format drifts from week to week, and the briefing competes with live work every Monday. When the operator is busy, the brief gets thinner or later — exactly when the principal most needs the overview. The difficulty is not judgment; it is the repeatable, structure-heavy assembly that crowds out higher-value work.

## Traditional workflow

The operator opens the calendar, the task list, and last week's notes in separate windows; copies the relevant items into a document; reorganizes them into sections; chases the open follow-ups; and edits the whole thing into the principal's preferred format. It takes a focused block of time, the format varies with how rushed the operator is, and follow-ups carried over from prior weeks are easy to drop.

## AI-assisted workflow

The operator runs the [Weekly Principal Briefing System](../blueprints/weekly-principal-briefing-system.md) blueprint, which composes three skills:

1. Run **[Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/)** on last week's meeting notes to surface decisions, owners, and the follow-ups that carry into this week.
2. Run **[Meeting Prep Pack](../skills/meeting-prep-pack/)** for the week's key upcoming meetings to produce a short prep list.
3. Run **[Principal Weekly Brief](../skills/principal-weekly-brief/)** to consolidate calendar, decisions awaiting the principal, investment and operational updates (summary only), vendor issues, and the carried-over follow-ups into one consistently formatted draft.

The AI assembles and structures; it does not decide what matters or send anything. The operator then reviews.

## Inputs

- Calendar items for the week (fictional or approved, non-confidential)
- Open decisions awaiting the principal
- Investment and operational updates, for summary only
- Open vendor or service issues
- Last week's meeting notes
- Follow-ups carried over from prior weeks
- Travel notes, if any

## Skills used

- [Principal Weekly Brief](../skills/principal-weekly-brief/) — the core briefing
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — prep for the week's key meetings
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — carrying last week's outcomes into this week's follow-ups

## Context sources

Manual input first: the operator pastes the relevant items. As the workflow earns trust, an office may add scoped, read-only connectors — for example, an approved calendar or task list — to reduce copy-and-paste. Connectors are optional, least-privilege, and read-only; they improve context but do not replace review. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Review gates

- **Inputs gate:** confirm sources are approved and contain no unapproved confidential material.
- **Pre-delivery gate:** a competent person verifies every fact, date, and figure against source, confirms that assumptions are labeled and missing items flagged, and edits framing before the principal sees it.
- **Delivery gate:** a person delivers the brief. The system never sends it.

## Outputs

- A weekly principal brief (draft)
- A decisions-needed list (draft)
- An upcoming-meetings prep list (draft)
- A carried-over follow-up list (draft)

## Measurement

How this workflow could be measured ([measurement framework](../docs/measurement-framework.md); figures are directional, not audited):

- **Time saved** — preparation time avoided per brief versus assembling by hand.
- **Cycle time reduced** — from "inputs available" to "reviewed brief ready."
- **Review exceptions** — instances where a brief was used without the required review (driven toward zero).
- **Follow-ups captured** — carried-over items surfaced rather than dropped.
- **Decisions supported** — decisions-needed items the principal acted on.
- **Documents summarized** — updates and notes folded into the brief.
- **Action items created** — owned follow-ups produced for the week.

## Risks and controls

- **Confidentiality** — the brief may touch sensitive matters; use only approved, non-confidential or fictional inputs in any public or unapproved tool, and an enterprise environment otherwise. See [privacy-and-confidentiality.md](../docs/privacy-and-confidentiality.md).
- **Stale information** — carried-over items can be presented as current; the reviewer confirms status against source before delivery.
- **Hallucination** — the AI may invent an update or a meeting not in the inputs; every fact is verified against source.
- **Professional advice boundary** — the brief summarizes; it makes no investment, legal, tax, or compliance recommendation.
- **Overreliance** — a fluent brief reads as authoritative; the reviewer treats it as an unverified draft, not a finished work product.

## What remains human

- Deciding what genuinely matters to the principal this week.
- Verifying every fact, date, and figure against source.
- Framing sensitive items and judgment calls.
- The actual decisions the brief surfaces.
- Managing the principal relationship and delivering the brief.

## Takeaway

The leverage is in consistency and recovered attention, not autonomy: the AI assembles a reliable draft every week so the operator spends their scarce time on judgment and framing, not on copying and reformatting — and a person still owns every fact and the final delivery.

---

*This case study is an illustrative operating pattern, not legal, compliance, investment, tax, or fiduciary advice, and not a live integration. Every output described is an unverified draft requiring human review.*
