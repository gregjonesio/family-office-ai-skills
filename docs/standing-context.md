# Standing Context: What an Office Has to Write Down

The workflows in this library repeatedly defer to something outside themselves. They say things like *retrieve the office's existing allocation policy rather than inventing one*, or mark an output *(missing)* because no chart of accounts, no matching tolerance, and no pending-item policy were provided.

Those deferrals are deliberate. A workflow that invents an accounting treatment is worse than one that refuses to. But they create a dependency, and this document names it: **the skills are only as useful as the standing context an office has actually written down.**

An office that runs a structured workflow with no written conventions gets *ask a person* on nearly every line and concludes the workflow does not work. It worked exactly as designed. What was missing was the layer underneath it.

---

## Two kinds of context, often confused

| | Run context | Standing context |
|---|---|---|
| **What it is** | What you provide for one task | What is always true about the office |
| **Examples** | A statement, a document, a feed export, meeting notes | Conventions, policy, entity structure, decisions and their reasons |
| **Lifespan** | One run | Until deliberately changed |
| **Failure mode** | Incomplete or stale input, one bad output | Wrong or absent substrate, *every* output quietly wrong |
| **Covered in** | [connectors-and-context.md](connectors-and-context.md) | This document |

Connector governance is about run context: what a workflow may reach for, and the data-access risk that creates. Standing context is a separate problem. A connector with perfect access to a system that contains no written conventions still cannot tell a workflow how this office treats a shared vendor cost.

## The four categories

**Conventions.** How this office does a recurring thing. Which account a category of transaction goes to, how a shared cost is split, what gets excluded and why, what tolerance is acceptable. These are the deferrals most workflows hit first.

**Structure.** What exists and how it relates. Entities, ownership, which accounts belong to which entity, who is responsible for what, the chart of accounts. Without this a workflow cannot tell an internal transfer from an external payment.

**Decisions.** What was chosen, when, and **why**. The reason matters more than the choice. A convention recorded without its reasoning gets relitigated every time someone new arrives, and worse, gets extended to cases it was never meant to cover.

**Institutional memory.** What happened and what was learned. Prior treatments, resolved ambiguities, things that turned out to be wrong. This is what keeps an office from solving the same problem three times.

## The minimum set for accounting routines

If you adopt nothing else, these are the ones the workflows in this library actually reach for:

- A **chart of accounts** with enough description that a category maps to an account without guessing.
- **Categorization conventions** for recurring transaction types, including what is deliberately excluded and why.
- An **entity and account map**: which accounts belong to which entity.
- **Allocation policy** for costs that benefit more than one entity, including the driver and the rounding rule.
- **Intercompany policy**: how movements between entities are recorded, and how they are expected to resolve.
- **Matching tolerances** for amount and date, or an explicit statement that none exist.
- **Period boundaries and any hard date floor**, such as a conversion date before which nothing should be recorded.
- **Who approves what**, at what threshold.

Most of that fits in one document. See [accounting-conventions-template.md](../templates/accounting-conventions-template.md).

## Ownership and maintenance

Standing context that nobody owns becomes standing context that nobody trusts.

- **Name an owner** for each document. Not a committee.
- **Date everything.** A workflow applying this year's convention to last year's transactions will be confidently wrong. If a convention changed, record when, so the right one can be applied to the right period.
- **State precedence.** When documents disagree, say which wins. A useful default: approved policy beats working notes, working notes beat conversation, and nothing beats a document nobody has read in two years without someone confirming it still holds.
- **Update in the same task that changes the practice.** Deferring the write-up to a later cleanup is how conventions and reality separate.
- **Review on a cadence**, and record the review. A convention nobody has looked at is not obviously current, whatever its date says.

## How standing context fails

These are the failure modes worth designing against. Most offices meet several.

**It lives in someone's head.** The convention is real, consistently applied, and written nowhere. It works until that person is unavailable, and then it does not exist. This is a continuity risk before it is an AI problem.

**A house convention is mistaken for a general truth.** An office adopts a treatment that is correct for its own structure and agreements, and it gets recorded as though it were universal. Then it is applied to a case where it does not hold, or published where someone else adopts it. Record the *scope* of a convention alongside the convention.

**The record captures intent instead of effect.** A note says a month was processed. That records what someone set out to do, not what actually landed. Standing context should assert observable state, not completed intentions, wherever it can.

**A summary goes stale faster than the thing it summarizes.** Index lines, overviews, and dashboards drift from the documents beneath them, and they are what people actually read. Treat a summary as a pointer, not as the fact.

**Two documents disagree and neither knows it.** Without a precedence rule, whoever reads first is right. This is why precedence has to be stated rather than assumed.

**It is not where the work happens.** Standing context stored somewhere nobody opens during the task will not be consulted during the task. Proximity beats completeness.

## What this is not

- **Not a data connector.** Access to systems is a separate concern with separate controls.
- **Not a substitute for judgment.** Written conventions make a workflow's deferrals resolvable; they do not make its output correct. Human review remains the control.
- **Not a reason to write everything down.** Aim for the conventions that recur. A document covering every case will not be maintained, and an unmaintained convention is worse than an absent one, because it is trusted.
- **Not confidential material for public tools.** Standing context often names entities, accounts, and structure. Treat it with the same care as the transactions it governs. See [privacy-and-confidentiality.md](privacy-and-confidentiality.md).

## Starting from nothing

Do not begin by writing policy. Begin by capturing what you already do.

1. Run a workflow and collect every item it returned as *(missing)* or *requires a person*.
2. Those are your undocumented conventions. Most already exist as consistent practice.
3. Write them down as they are, with dates and the reason for each.
4. Re-run. The deferrals that remain are genuine open questions, and now you can see them.

The list of things a workflow could not resolve is the most accurate inventory of missing standing context an office is likely to get.

---

*This document is operational guidance, not legal, compliance, accounting, investment, or cybersecurity advice, and creates no professional relationship. Written conventions make a workflow's output more consistent and easier to review; they do not make it correct, and they are not a control. A competent person remains accountable for every output and for the conventions themselves.*
