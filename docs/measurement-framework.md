# Measurement Framework

A practical way to measure whether AI workflows are actually helping a family office or RIA, and to do so honestly. The framework is built around the idea of an AI-native family office operating system: a set of governed, repeatable workflows whose value should be observable, not assumed.

A warning up front: the easiest numbers to produce (hours saved, dollar value) are the easiest to overstate. This framework is for internal management insight, not for marketing claims or audited reporting. Treat every value figure as **directional**.

---

## What to measure

Group metrics into activity, efficiency, quality/governance, and value. Activity and efficiency tell you whether the workflows are used and faster. Quality and governance tell you whether they are used *safely*. Value is the most fragile and should be reported with the most caution.

### Activity metrics

| Metric | Definition |
|--------|------------|
| Workflows created | Distinct skills/workflows adopted by the office |
| Workflows executed | Count of skill runs over a period |
| Documents summarized | Documents processed via the document digest workflow |
| Meetings prepared | Meeting prep packs produced |
| Action items extracted | Action items captured from meetings |
| Decisions supported | Briefs/memos prepared to support a decision (not decisions made by AI) |
| Follow-ups drafted | Internal follow-up drafts produced for human review |
| Knowledge assets produced | Durable digests, records, and summaries retained as institutional memory |

### Efficiency metrics

| Metric | Definition |
|--------|------------|
| Hours saved (estimated) | Estimated preparation time avoided, by workflow |
| Cycle time reduced | Change in elapsed time from input to a review-ready draft |
| Systems connected | Count of governed, approved tools/environments in use (not live integrations) |

### Quality and governance metrics

| Metric | Definition |
|--------|------------|
| Human-review completion rate | Share of outputs that received required human review before use |
| Review exceptions | Outputs used without the required review (should trend to zero) |
| Correction rate | Share of reviewed drafts that needed a fix before they could be used, reported with the number reviewed and the number with no answer recorded (see below) |
| Confidentiality incidents | Instances of sensitive data handled in an unapproved tool (target: zero) |

The governance metrics matter most. A workflow that "saves time" while skipping review is not a success: it is an unmanaged risk.

### Recording the correction rate

Human-review completion and review exceptions record whether the required review happened. Neither records what the review changed. A reviewer can open a draft, correct a wrong figure, pass it on, and leave no trace of having done it; the finished document and the quarterly report both look the same whether the review changed nothing or fixed three things. The correction rate is the measure that tells them apart, so it belongs on every workflow's list, not only the pilot's.

- **Agree in advance what counts.** A fix is a change the reviewer had to make before the work could be used: a wrong figure, a missing item, a passage that would have misled the reader. A phrase the reviewer would have written differently is not a fix.
- **Record one answer per reviewed draft.** Yes or no. Report the share marked yes, the number of drafts reviewed, and the number where nobody recorded an answer. The blanks are part of the measure, and at first most drafts will have no answer at all.
- **The reviewer decides.** An AI can add up the answers and lay out the report. Whether a change counted as a fix is the reviewer's call, not the AI's, and an AI's opinion of its own draft is not evidence.
- **Read it with its limits.** The count includes only what the reviewer caught, never what was missed. A rising rate does not tell you the cause: the inputs may have changed, the work may have drifted into cases the workflow was never set up for, a new reviewer may apply a different standard, or the drafts may be worse. A falling rate is equally consistent with reviewers who stopped recording. Report it next to hours saved, not instead of it, and use it to decide where to look, not to grade the tool.

### Value metrics (handle with care)

| Metric | Definition |
|--------|------------|
| Estimated value created | A directional estimate of time value, defined below |

## A suggested value estimate, and its limits

A simple, transparent estimate:

```
Estimated value = estimated hours saved × blended hourly rate
```

Use a conservative blended rate and conservative time estimates. Then read the caveats, which matter more than the number:

- It is **directional, not audited.** It is an internal estimate, not a financial metric.
- It **does not capture decision quality:** better preparation may or may not lead to better decisions.
- It **does not capture avoided errors:** value from catching a missed date or a bad term is real but unmeasured here.
- It **does not prove ROI:** it ignores tool costs, training, review time, and risk.
- It **must not be represented as audited savings** or as a financial return.

State these caveats wherever the figure appears. A clean number with no caveat is exactly how directional estimates become overstated claims.

## How to use this framework

1. **Start small.** Track a few metrics for your pilot workflow rather than all of them.
2. **Prioritize governance metrics.** Human-review completion, correction rate, and confidentiality incidents are the ones that protect the office.
3. **Estimate conservatively.** When in doubt, understate hours saved and value.
4. **Review the trend, not the point.** Direction over time is more useful than any single figure.
5. **Keep value figures internal and caveated.** Do not put an uncaveated dollar figure in front of a principal, client, or the public.

## What this framework does not do

- It does not prove return on investment.
- It does not measure decision quality or avoided losses.
- It does not produce audited or financial-statement figures.
- It does not substitute for judgment about whether a workflow is worth keeping.

---

*This framework is for internal management insight only. Value estimates are directional and unaudited, and are not financial, investment, or accounting advice.*
