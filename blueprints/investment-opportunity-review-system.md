# Blueprint: Investment Opportunity Review System

A composed system for moving an inbound opportunity through a consistent first-pass review, diligence question development, and meeting follow-through — without ever recommending, approving, or sizing an investment. This is a **design pattern**, not an automation. Read-only, human-in-the-loop, non-advisory. It does not replace diligence, an investment committee, or professional advice.

---

## Purpose

Standardize the front of the deal funnel so every opportunity receives the same disciplined first-pass treatment: a structured screen, the right diligence questions, a clear list of what is missing, and prepared follow-through — all as drafts for human judgment.

## When to use

- Triaging inbound deal flow into a consistent format.
- Preparing material for an investment committee or principal to react to.
- Developing diligence question sets and tracking what is missing.

## Inputs

- Deal summary, deck notes, CIM excerpt, or founder email
- Manager/fund materials where relevant (deck, DDQ, factsheet)
- Prior questions and notes
- Meeting notes from calls with the opportunity

## Context sources

Manual input first; approved read-only connectors where appropriate. Possible sources: approved deal notes, pitch materials, a diligence tracker, meeting notes, and prior questions. Treat all retrieved claims as unverified. Confirm the AI environment is approved for confidential deal material. See [connectors-and-context.md](../docs/connectors-and-context.md).

## Skills used

- [Investment Memo Screener](../skills/investment-memo-screener/) — first-pass memo
- [Manager Diligence Summarizer](../skills/manager-diligence-summarizer/) — where a fund/manager is involved
- [Meeting Prep Pack](../skills/meeting-prep-pack/) — prep for diligence calls
- [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) — capture follow-ups

## Workflow sequence

1. Gather source material (manual or approved read-only retrieval).
2. Run **Investment Memo Screener** → first-pass memo separating the promoter's thesis from verified fact.
3. Where a manager/fund applies, run **Manager Diligence Summarizer** → diligence-ready summary.
4. Run **Meeting Prep Pack** for the diligence call → questions and background.
5. After the call, run **Post-Meeting Action Extractor** → follow-ups and open questions.
6. **Human review gate** → verify facts; route to the office's diligence/committee process.

## Human review gates

- **Gate 1 — Inputs:** confirm the environment is approved for this material; no unapproved confidential data.
- **Gate 2 — Memo review:** a competent person verifies every figure and claim against source, confirms the memo makes no recommendation, and checks the missing-information list.
- **Gate 3 — Process:** the opportunity enters the office's normal diligence and investment-committee process; the system does not shortcut it.

## Outputs

- First-pass memo
- Diligence questions
- Missing-information list
- Next-meeting prep
- Follow-up action list

## Measurement metrics

- Opportunities screened in a consistent format
- Human-review completion rate (target: 100%)
- Share of opportunities with a complete missing-information list before advancing
- Estimated analyst time saved (directional)

See [measurement-framework.md](../docs/measurement-framework.md). Value figures are directional only.

## Failure modes

- Treating the promoter's thesis as verified fact
- Supplying market sizes, comparables, or figures not in the source
- Advice creep into "should we invest" territory
- Compressed timelines pressuring review to be skipped
- Relying on a manager's unverified track record

## Prohibited actions

- Do not recommend investing.
- Do not approve allocation.
- Do not provide fiduciary advice.
- Do not rely on unverified claims.
- Do not bypass the investment committee or review process.
- No investment, legal, or tax advice; no position sizing.

## Implementation notes

Begin with manual input on a few real (sanitized) opportunities. Keep the screener's "no recommendation" behavior under adversarial test (see [evals](../evals/)). Never let a fast-moving deal justify skipping verification or committee process.

---

*This blueprint is an operational design pattern, not investment, legal, tax, or fiduciary advice, and not a live integration. It makes no recommendation to invest. Every output is an unverified draft requiring human review and the office's normal diligence process.*
