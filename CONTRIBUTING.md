# Contributing

Thank you for considering a contribution. This repository exists to give family office and wealth management operators a credible, reusable library of AI workflows. Good contributions make the workflows clearer, safer, and more useful in real operating environments.

## What we welcome

- **New skills** that follow the standard `SKILL.md` format and fill a genuine operational gap.
- **Improvements to existing skills** — clearer instructions, better quality-control checks, stronger guardrails.
- **New or improved templates** for common family office artifacts.
- **Documentation** that helps operators implement and govern AI responsibly.
- **Better examples** — sanitized, realistic sample inputs and outputs.

## Hard requirements

Every contribution **must** meet all of the following. Pull requests that do not will be declined.

- **No confidential information.** Nothing real about any family, principal, employer, client, employee, vendor, counterparty, entity, or investment.
- **No employer-, client-, or principal-specific data.** Examples must be fully fictional and clearly generic. This includes real principal or family information, real investment data, confidential documents, and live system details.
- **No implied affiliation or endorsement.** Do not suggest that a workflow was built for, used at, approved by, sponsored by, or extracted from any employer, client, principal, or named family office.
- **No live credentials, secrets, keys, tokens, endpoints, or account identifiers.**
- **No investment recommendations.** Skills support analysis and preparation; they do not tell anyone what to buy, sell, hold, or allocate.
- **No legal, tax, accounting, or compliance advice.** Workflows may prepare questions *for* advisers; they must not substitute for them.
- **No autonomous action.** Nothing that sends communications, executes transactions, approves commitments, or connects to live financial systems without explicit human review.
- **Professional, institutional tone.** Understated and practical. Avoid hype, buzzwords, and exaggerated claims.

## Style guidelines

- Write in clean, well-structured Markdown.
- Use tables where they improve clarity.
- Keep language precise and operator-oriented.
- Avoid excessive emojis.
- Prefer plain English over jargon; define terms when you must use them.
- Match the structure of existing skills and templates so the library stays consistent.

## Adding a new skill

1. Create a folder under `skills/` using a clear, kebab-case name.
2. Add a `SKILL.md` that follows the standard format used by the existing skills:
   - YAML front matter with `name` and `description`
   - `Purpose`, `When to use this`, `Inputs`, `Output`, `Instructions`, `Quality control`, `Do not`, `Example request`
3. Add a `README.md` with a plain-English overview.
4. Add an `examples/` folder with `sample-input.md` and `sample-output.md`, using fully fictional data.
5. Confirm the skill enforces the universal behavioral rules: do not invent facts, separate confirmed information from assumptions, flag missing information, preserve confidentiality, give no professional advice, and recommend no transaction.

## Submitting

1. Fork the repository and create a feature branch.
2. Make your changes following the requirements above.
3. Open a pull request with a clear description of what you changed and why.
4. Confirm in the PR description that your contribution contains no confidential information, no client data, and no live credentials.

By contributing, you agree that your contributions are licensed under the repository's [MIT License](LICENSE).
