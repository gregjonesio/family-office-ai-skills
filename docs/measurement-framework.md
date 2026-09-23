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
| Correction rate | Share of reviewed drafts with a recorded outcome that needed a material correction before use, reported with the total reviewed and the number with no answer recorded (see the section below) |
| Confidentiality incidents | Instances of sensitive data handled in an unapproved tool (target: zero) |

The governance metrics matter most. A workflow that "saves time" while skipping review is not a success: it is an unmanaged risk.

### Recording the correction rate

Human-review completion and review exceptions show whether the required review happened. They cannot show whether the review changed anything: a review that changed nothing and one that corrected a wrong figure count the same. Correction rate is the measure that tells them apart, so it belongs on every workflow's list, not only the pilot's.

- **Agree in advance what counts.** A material correction is a change needed before the work could be used: a wrong figure corrected, a required item added, misleading wording removed. A change made only for stylistic preference does not count. Define the output being counted before recording begins, and count each output's initial review once.
- **Record one answer per reviewed draft.** Yes, no, or not recorded. Mark yes when the reviewer identified a material correction, including when the draft was rejected rather than revised. The correction rate for a period is the number marked yes divided by the number marked yes or no. Report it with the total reviewed and the number with no answer recorded; if no answers were recorded, report the rate as unavailable rather than as zero.
- **The reviewer decides.** An AI may help tally the recorded answers and lay out the report. Whether a material correction was needed is the reviewer's determination, and an AI's assessment of its own draft does not replace it.
- **Read it with its limits.** The rate reflects only the corrections reviewers identified, never what was missed, and it records whether a correction was needed, not how much rework it took. A change in the rate may reflect differences in inputs, task difficulty, review standards, recording practice, or draft quality. Read it alongside the unrecorded count and review burden; a lower rate alone does not establish better quality.

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
