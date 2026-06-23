# Roadmap

A conservative, public view of where this library is going. The priority is depth, trust, and repeatability — not feature count. Some things are deliberately **not** planned, and that list matters as much as the rest.

This roadmap is directional and may change. Nothing here is a commitment or a timeline.

---

## Current focus

- Strengthening the structure, governance, and safety layer around the existing seven skills.
- Documentation that helps operators adopt AI responsibly: governance, privacy, threat model, evaluation, measurement, and the maturity model.
- Keeping the library conservative, sanitized, and non-executable by default.

## Advanced operator layer

Included in v0.1.0. These move the repository beyond a skill library toward a public blueprint for an AI-native family office operating layer — all read-only, human-in-the-loop, and non-executable:

- [Reference architecture](docs/reference-architecture.md) — the six-layer model.
- [AI Workforce operating model](docs/ai-workforce-operating-model.md) — definition, vocabulary, and what stays human.
- [Skill maturity matrix](docs/skill-maturity-matrix.md) — prompt to operating layer.
- [System blueprints](blueprints/) — composed, end-to-end workflow designs.
- [Non-executable evaluation examples](evals/) — red-team scenarios for conservative behavior.

## Near-term improvements

- Refining the existing skills' instructions and quality-control checks based on feedback.
- Expanding evaluation and red-team coverage for each skill.
- Improving examples and templates for clarity.
- Tightening the catalog and schema as the library grows.

## Future skill categories

Potential areas for future skills, all subject to the same read-only, human-in-the-loop, no-advice posture. Listing a category is not a commitment to build it.

- Investment operations
- Principal reporting
- Entity administration
- Insurance review (summary and question preparation only)
- Vendor and aviation operations support
- Philanthropy workflow support
- Household and property administration
- Document management
- RIA operations

Each new skill would ship with a `SKILL.md`, a plain-English README, fictional examples, a catalog entry, and a disclaimer — following the [skill design principles](docs/skill-design-principles.md).

## Not currently planned

These are out of scope by design. They would conflict with the repository's safety posture.

- Live trading or order placement
- Autonomous communications (auto-sending email or messages)
- Transaction approval or commitment authority
- Tax, legal, accounting, or compliance advice
- Portfolio or allocation recommendations
- Integrations with live or confidential systems
- Executable code, scripts, or automation as a default part of the repository
- Anything that removes the human from a consequential decision

If your need falls into this list, this library is intentionally not the right tool for it.

---

*This roadmap is informational only and is not a commitment, a product plan, or professional advice.*
