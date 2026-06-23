# Changelog

All notable changes to this repository are documented here. This project follows
[Keep a Changelog](https://keepachangelog.com/) conventions and
[Semantic Versioning](https://semver.org/) where applicable.

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
