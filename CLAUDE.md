# CLAUDE.md — Standing Instructions for AI Coding Sessions

These are durable instructions for any Claude Code (or other AI coding agent) session that edits this repository. Read this file before making changes. If a request conflicts with the rules here, follow these rules and surface the conflict to the user.

## Repository purpose

`family-office-ai-skills` is a **public, open-source** library of structured AI skills, prompts, workflow templates, and governance documentation for lean single-family offices, multi-family offices, registered investment advisers (RIAs), and wealth operators. The skills are read-only, judgment-support workflows that produce drafts for human review. The repository is **non-executable by default** — documentation and markdown, not running code.

## Repo identity

This repository should remain:

- independent
- public-facing
- operator-led
- model-agnostic
- read-only by default
- human-in-the-loop
- non-advisory
- useful without private context
- unaffiliated with any employer, client, principal, or family office unless explicitly authorized in writing

Future Claude Code sessions should **not** turn it into:

- a software product
- a sales funnel
- an automation framework
- a live integration repo
- a legal/compliance/investment advice system
- an employer-specific or client-specific repository
- a public representation of any private operating system

It is created by Greg Jones from generalized operator experience. Keep attribution independent: never imply it was built for, used at, approved by, or extracted from any employer, client, principal, or named family office.

## Audience

Two audiences, both addressed:
- **Operators** — single/multi-family office staff, RIAs, investment analysts, chiefs of staff, executive assistants, wealth operations teams.
- **AI builders** — engineers adapting the `SKILL.md` specifications into their own assistants, agents, or tooling.

## This is a public-facing repository

Treat everything you add as if it will be read by the public, competitors, regulators, and journalists. **Never add:**
- Confidential family office information of any kind.
- Real names, companies, deals, principals, vendors, counterparties, or entities.
- Client-specific or proprietary data.
- Live credentials, API keys, tokens, secrets, endpoints, or account identifiers.
- Transaction authority, autonomous actions, or live system integrations.
- Investment, legal, tax, accounting, compliance, cybersecurity, or fiduciary advice.

All examples and sample data must be **fully fictional and clearly generic.**

## Tone rules

Professional, understated, practical, operator-led. Avoid hype, buzzwords, and exaggerated claims. Prefer plain English; define terms when needed. Do not make economic, performance, or reliability claims that cannot be substantiated. Match the voice of the existing files.

## Safety rules

- **Read-only by default.** Skills support judgment; they never decide, transact, approve, or send.
- **Human review is required.** Every output is an unverified draft for a competent person to verify.
- **Guardrails are instructions, not guarantees.** Never imply that a skill's `Do not` list or quality-control checks are enforceable controls. They are prompt-level instructions an AI may not follow perfectly. Human review is the real control.
- **Do not imply AI outputs are reliable.** Do not describe output as "safe," "compliant," "accurate," or "verified."
- **Preserve all disclaimers.** Do not weaken, remove, or shorten disclaimers in any file. New skills and docs must carry equivalent disclaimers.

## Confidentiality rules

- Never introduce real sensitive data, even as an "example."
- Sample inputs/outputs use placeholders (`[Principal]`, `[Entity A]`, "the Fund," "the custodian") and invented scenarios.
- Do not reference the maintainer's real holdings, vendors, or operations.

## Prohibited content (hard stops)

- Anything that approves, executes, or recommends a transaction or allocation.
- Anything that sends communications automatically.
- Anything that provides professional advice (investment, legal, tax, accounting, compliance, fiduciary, cybersecurity).
- Anything that connects to live systems or stores credentials.
- Scripts, GitHub Actions, package manifests, or other executable code — **unless the user explicitly approves it.** The repository is non-executable by default.

## File conventions

```
skills/<skill-id>/SKILL.md          Workflow contract (YAML front matter + standard sections)
skills/<skill-id>/README.md         Plain-English overview
skills/<skill-id>/examples/         sample-input.md and sample-output.md (fictional)
skills/catalog.yaml                 Machine-readable catalog of all skills
schemas/                            JSON schema documentation (no enforcement scripts)
templates/                          Reusable markdown artifact templates
docs/                               Governance, safety, and operating-model documentation
```

`SKILL.md` front matter uses `name` and `description`. The body uses, in order: `Purpose`, `When to use this`, `Inputs`, `Output`, `Instructions`, `Quality control`, `Do not`, `Example request`, and a closing disclaimer footer.

## Required disclaimer posture

Every skill, template, doc, and sample output must make clear, in its own text, that it:
- supports human judgment and produces drafts, not decisions;
- is not investment, legal, tax, accounting, compliance, or cybersecurity advice;
- requires human verification;
- creates no professional or fiduciary relationship.

If you add a file that could be mistaken for advice or for an authoritative control, add the disclaimer.

## How to add a new skill

1. Create `skills/<kebab-case-id>/`.
2. Add `SKILL.md` in the standard format, including a `Do not` section, a `Quality control` section, and a disclaimer footer.
3. Add `README.md` (plain-English overview).
4. Add `examples/sample-input.md` and `examples/sample-output.md` using fully fictional data; the sample output must model conservative behavior (flag missing info, separate facts from assumptions, no advice, no recommendation).
5. Add a corresponding entry to `skills/catalog.yaml` with conservative metadata (`tool_permissions: none`, `human_review_required: true`, complete `prohibited_actions`).
6. Confirm the entry validates against `schemas/skill-manifest.schema.json`.
7. Follow [docs/skill-design-principles.md](docs/skill-design-principles.md).

## Review checklist before any commit

Confirm all of the following before proposing a commit:

- [ ] No confidential information or real names/entities/deals/vendors.
- [ ] No client-specific or proprietary data.
- [ ] No live credentials, keys, tokens, or endpoints.
- [ ] No investment, legal, tax, accounting, compliance, or fiduciary advice.
- [ ] No transaction authority, autonomous actions, or live integrations.
- [ ] No executable code added without explicit user approval.
- [ ] All sample data is fictional.
- [ ] Disclaimers preserved and present on new material.
- [ ] Guardrails described as instructions, not guarantees.
- [ ] Tone is professional and non-promotional.
- [ ] `skills/catalog.yaml` updated if skills changed.
- [ ] Do not commit or push without the user's explicit approval.
