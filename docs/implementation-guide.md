# Implementation Guide

A step-by-step guide for putting these skills to work inside a small family office or RIA. The aim is to capture real operating leverage quickly while managing the confidentiality and governance risks that come with using AI. You do not need a large team or a technology budget to start — you need one good pilot, clear rules, and a habit of review.

---

## Overview

A sensible rollout moves through five stages:

1. **Set the guardrails** — governance and privacy before usage.
2. **Pick one pilot workflow** — a single, high-frequency, low-risk task.
3. **Train the people who will use it** — boundaries first, mechanics second.
4. **Build the review loop** — human verification baked into the process.
5. **Measure and expand** — prove value, then add the next workflow.

Resist the urge to roll out everything at once. One workflow done well builds the trust and habits that make the next five easier.

## Step 1 — Set the guardrails first

Before anyone uses AI for office work, put two things in place:

- **Governance boundaries.** Read and adapt [ai-governance-for-family-offices.md](ai-governance-for-family-offices.md). Decide approved uses, prohibited uses, your approved tool(s), and who owns AI use.
- **Privacy rules.** Read and adapt [privacy-and-confidentiality.md](privacy-and-confidentiality.md). Confirm you have an enterprise environment with acceptable data terms, and brief the team on what must never be pasted into public tools.

This step is non-negotiable and takes a few hours, not weeks. Skipping it is how offices get into trouble.

## Step 2 — Choose your pilot workflow

Pick **one** workflow with these properties:

- **High frequency** — you do it weekly or more, so the leverage compounds.
- **Structure-heavy** — the value is in organizing information, not in judgment.
- **Low consequence on first draft** — a mistake in the draft is caught in normal review.
- **Owned by one person** — a single user can run the pilot end to end.

Good first pilots:

| Pilot | Why it works |
|-------|--------------|
| [Principal Weekly Brief](../skills/principal-weekly-brief/) | High frequency, clear inputs, reviewed every week anyway |
| [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) | Immediate time savings, easy to verify against notes |
| [Document Digest](../skills/document-digest/) | Obvious value, with counsel still reviewing the source |
| [Meeting Prep Pack](../skills/meeting-prep-pack/) | Standardizes prep, low risk, fast feedback |

Avoid starting with the highest-stakes workflows (investment screening, manager diligence) until the team has built review habits on something lower-consequence.

## Decide how context enters the workflow

Before you scale, decide how information will reach the workflow.

- **Start with manual input.** For pilots, paste fictional or approved, non-confidential material. This is the lowest-risk way to learn how a skill behaves.
- **Read-only connectors can reduce copy/paste** once a workflow has earned trust — for example, retrieving an approved calendar or document for a brief.
- **Connectors should be approved and scoped** to the minimum necessary (least privilege), read-only first, with no autonomous write, send, or transaction.
- **Do not connect live confidential systems without governance** — approval, access controls, logging, revocation, and human review must be in place first.

Connectors are optional and are not required to use these skills. They improve context; they do not replace human review or reduce confidentiality risk. See [connectors-and-context.md](connectors-and-context.md) for the full operating model, maturity levels, and approval checklist.

## Step 3 — Train the people who will use it

Training is short but should cover, in order:

1. **The boundaries.** Approved uses, prohibited uses, and the privacy rules — before any mechanics.
2. **The failure modes.** Confident inaccuracy, stale information, and over-trusting fluent output. Show an example of the AI being wrong so the team internalizes the need to verify.
3. **The mechanics.** How to gather inputs, invoke the skill (each skill's *Example request*), and read the output as a draft.
4. **The review standard.** What "reviewed" means for this workflow, and who is accountable.

Keep it practical. A 60-to-90-minute working session on a real example beats a slide deck.

## Step 4 — Build the review loop

Make human verification part of the process, not an afterthought.

- **Define the reviewer and the standard** for the pilot. For a principal brief, the reviewer checks facts and framing; for a document digest, counsel still reviews the underlying document.
- **Run input → draft → review → use.** The AI produces the draft; a competent person verifies material facts against source; only then is it used.
- **Capture corrections.** When the reviewer fixes something, note the pattern. Recurring corrections usually mean the input was incomplete or the skill's instructions need tuning for your house style.
- **Never let output skip review on a busy day.** The discipline matters most exactly when time is short.

## Step 5 — Measure

Track a few simple, honest measures so you can decide whether to expand:

| Measure | Question it answers |
|---------|--------------------|
| Time saved per run | Is this actually faster than doing it by hand? |
| Review burden | How much correction does each draft need? |
| Error rate caught in review | Is quality acceptable and trending the right way? |
| Adoption | Is the team actually using it, or quietly avoiding it? |
| Principal/stakeholder feedback | Is the output genuinely useful and well-framed? |

A workflow is working when it saves meaningful time, needs steadily less correction, and the team reaches for it without being told to.

## Step 6 — Expand deliberately

Once the pilot is delivering value with an acceptable review burden:

- **Add one workflow at a time.** Repeat steps 2–5 for the next skill.
- **Standardize the artifacts.** Adopt the [templates](../templates/) so output is consistent across the team.
- **Raise the stakes gradually.** Move toward higher-consequence workflows (diligence, screening) only after review habits are strong.
- **Document your house versions.** As you tune skills to your office, keep your adapted versions under version control with the same confidentiality discipline.

## A realistic first 30 days

| Week | Focus |
|------|-------|
| Week 1 | Set governance and privacy guardrails; confirm approved environment |
| Week 2 | Choose pilot; train the owner; run it alongside the manual process |
| Week 3 | Rely on the AI draft with full review; capture corrections and tune inputs |
| Week 4 | Review measures; decide whether to expand; document the house version |

## Common pitfalls

- **Skipping the guardrails** to "just try it" — this is how confidential data ends up in the wrong tool.
- **Starting with the hardest workflow** before review habits exist.
- **Treating output as finished** instead of as a draft.
- **Rolling out to everyone at once** before anyone has proven the loop.
- **Not measuring**, so the office can't tell value from novelty.

---

*This guide is operational, not legal, compliance, or regulatory advice. Adapt the rollout to your structure and obligations with qualified advisers.*
