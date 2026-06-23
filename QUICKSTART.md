# Quickstart

Run your first skill in under five minutes. No setup, no code, no accounts to connect — these are structured instructions you give to a capable AI assistant.

## What this repo is

A practical, operator-built starter kit of reusable AI **workflows** for lean family offices, RIAs, and wealth operators. Each skill is a structured set of instructions that turns scattered inputs into a clean, decision-ready *draft* for a human to review.

## What it is not

- It is **not** a decision-maker. It drafts and structures; it does not decide, recommend, transact, or send.
- It is **not** professional advice. Nothing here is investment, legal, tax, accounting, compliance, or fiduciary advice.
- It is **not** a live integration or an automation. It is read-only and human-in-the-loop by design.

> **Warning — confidentiality.** Do not paste confidential family, investment, legal, tax, health, account, entity, or personally identifiable information into public or unapproved AI tools. For your first run, use the fictional sample below or your own clearly non-confidential, de-identified input. See [Privacy and Confidentiality](docs/privacy-and-confidentiality.md).

---

## Five steps

### Step 1 — Choose a workflow

Start with **[Principal Weekly Brief](skills/principal-weekly-brief/)** — the simplest, highest-frequency workflow. It turns a week's calendar, decisions, and updates into a concise briefing draft.

### Step 2 — Copy the skill instructions

Open [`skills/principal-weekly-brief/SKILL.md`](skills/principal-weekly-brief/SKILL.md) and copy its contents into your AI assistant. That file is the workflow contract — it tells the assistant the inputs, the output structure, and the rules it must follow.

### Step 3 — Provide fictional or approved, non-confidential input

Paste the skill instructions, then add your inputs. For a first run, use this fictional sample:

```
Week of: Monday, March 9 – Friday, March 13

Calendar:
- Tue 10:00 — Intro call with a prospective co-investment sponsor
- Wed 14:00 — Quarterly review with the outsourced CIO
- Thu — Travel to second residence (afternoon)

Open decisions:
- Renew the property & casualty insurance program (quote up ~9%); broker wants direction by Friday.
- Optional follow-on for an existing venture fund (capital call received).

Operational issues:
- New entity formation paperwork pending counsel review.
- Disputed IT/AV vendor invoice — amount higher than agreed scope.

Pending follow-ups:
- Confirm updated beneficiary designations with estate counsel.
- Schedule annual household cybersecurity review.
```

The full versions are here: [sample input](skills/principal-weekly-brief/examples/sample-input.md) · [sample output](skills/principal-weekly-brief/examples/sample-output.md).

### Step 4 — Review the output manually

Read the draft as a draft. Check that it:

- used only the information you provided (invented nothing),
- separated confirmed facts from assumptions,
- flagged missing information instead of guessing, and
- made no recommendation or professional-advice statement.

Verify every fact against source. The output is a starting point for a person, never a final answer.

### Step 5 — Adapt internally, only after review

Once you have run it on fictional input and confirmed it behaves conservatively, adapt it to your own house style and recordkeeping — inside an approved, non-public environment with appropriate data-handling terms. Use the [templates](templates/) for consistent output, and see the [Implementation Guide](docs/implementation-guide.md) for a real rollout.

---

## Next steps

- Browse [the seven skills](README.md#the-skills).
- Read the [Trust and safety posture](README.md#trust-and-safety-posture).
- Test conservatively with the [Evaluation and Red-Team Guide](docs/evaluation-guide.md).

*This quickstart helps you try a skill safely. It is not professional advice, and human review is required for every output.*
