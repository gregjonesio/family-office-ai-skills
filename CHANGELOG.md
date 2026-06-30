# Changelog

All notable changes to this repository are documented here. This project follows
[Keep a Changelog](https://keepachangelog.com/) conventions and
[Semantic Versioning](https://semver.org/) where applicable.

## [Unreleased]

### Added

- **Operating Playbooks** (`playbooks/`): a new top-level section documenting how
  recurring family office responsibilities are executed and where AI reduces
  administrative burden while human review stays the primary control. Includes a
  `README.md`, a `PLAYBOOK-TEMPLATE.md`, and ten playbooks — principal weekly
  review, capital call processing, investment opportunity intake, board and
  committee meeting preparation, executive travel coordination, insurance renewal
  management, vendor onboarding and review, quarter-end close, entity governance
  calendar, and document review for counsel. Each follows the same structure,
  separates AI assistance from human responsibility, contains explicit review
  gates, and cross-links the relevant skills, blueprints, case studies, and
  governance documents. Read-only, human-in-the-loop, non-advisory, and
  non-executable, consistent with the rest of the repository.
- Each playbook carries substantive family office operating detail — institutional
  controls such as segregation of duties, dual authorization, independent
  out-of-band verification, authorized-signer matrices, and recurring governance
  calendars — written so an experienced operator learns how the process is run
  safely even without using AI. Every playbook includes a **Common Failure
  Points** section covering how the process breaks in practice and the control
  that prevents each failure, and an **Evolution Path** section describing how the
  process matures from ad hoc to institutionalized.

## [0.1.0] - Initial public draft

The first public draft of Family Office AI Skills: an open-source library of
read-only, human-in-the-loop AI workflows for lean family offices, RIAs, and
wealth operators.

### Added

- **Seven initial skills**, each with a `SKILL.md` contract, a plain-English
  README, and fictional sample input/output:
  - Principal Weekly Brief
  - Investment Memo Screener
  - Manager Diligence Summarizer
  - Meeting Prep Pack
  - Post-Meeting Action Extractor
  - Vendor Review
  - Document Digest
- **Governance and safety documentation**: AI governance guide, privacy and
  confidentiality rules, implementation guide, operating model, threat model,
  evaluation and red-team guide, measurement framework, AI maturity model, and
  skill design principles.
- **Reusable templates** for weekly briefs, investment memos, manager diligence,
  meeting prep, and action items.
- **Structure for AI builders**: a machine-readable skill catalog
  (`skills/catalog.yaml`) and a JSON schema (`schemas/skill-manifest.schema.json`)
  documenting conservative skill metadata. No enforcement scripts; the repository
  is non-executable by default.
- **Repository governance**: `CLAUDE.md` standing instructions for AI coding
  sessions, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, issue
  templates, a pull request template, and a roadmap.

### Safety posture

- All skills are read-only, human-in-the-loop, and judgment-support only.
- No skill grants tool permissions, transaction authority, or autonomous action.
- No executable code, live integrations, or credentials are included.
- Guardrails are documented as instructions to the AI, not enforceable controls.
- Disclaimers throughout: not investment, legal, tax, accounting, compliance,
  cybersecurity, or fiduciary advice.
- All examples use fully fictional, generic data.

[0.1.0]: https://github.com/gregjonesio/family-office-ai-skills/releases/tag/v0.1.0
