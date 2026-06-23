# Security Policy

## Scope of this repository

This repository contains **documentation, markdown templates, and structured AI workflow instructions**. By default it contains **no executable code** — no scripts, no application logic, no automation that runs on its own. There is nothing here that connects to a live system, sends a message, moves money, or executes a transaction.

That design is intentional. The skills are read-only, judgment-support workflows, with **no live integrations and no credentials** anywhere in the repository. The security surface of the repository itself is therefore small. The meaningful risk is not in the files — it is in **how you use them**. For a fuller treatment of the risks and the practices that reduce them, see the [Threat Model](docs/threat-model.md).

**Prompt guardrails are not security controls.** The `Do not` lists and quality-control checks inside each skill are written instructions to an AI model. They are not enforced by code, cannot be relied upon to prevent unsafe output, and must never be treated as a security boundary. Human review is the control.

## Using these materials safely

- **Do not connect these templates or skills to live systems without review.** If you adapt a skill into an automated pipeline, an agent, or an integration that can read from or write to a real system (email, custodian, accounting, CRM, document store, payment rails), have that integration reviewed by someone accountable for security and compliance before it touches production data.
- **Keep human review between AI output and any consequential action.** Nothing here is designed to act autonomously. Do not wire these workflows to anything that approves, commits, transacts, or sends without a person in the loop.
- **Treat skill guardrails as instructions, not technical controls.** The *Do not* lists and quality-control checks inside each skill are written instructions to the AI. They are not enforced by code, and a model may not follow them perfectly. Human review remains the control that prevents an unsafe output from becoming an unsafe action — do not rely on the prompt alone.
- **Handle confidential data appropriately.** Do not paste confidential family, client, entity, or counterparty information into public or consumer AI tools. Use an enterprise environment with appropriate data-handling and retention terms. See [docs/privacy-and-confidentiality.md](docs/privacy-and-confidentiality.md).
- **Treat all output as unverified.** AI output can be confidently wrong. Verify every figure, date, name, and claim against source documents before relying on it.
- **Manage credentials outside this repository.** Never store API keys, tokens, passwords, or other secrets in files derived from these templates.

## Reporting a problem

If you discover a security or privacy concern related to this repository — for example, content that inadvertently exposes sensitive information, a template that encourages an unsafe practice, instructions that could be mistaken for professional advice, content implying autonomy or transaction authority, a suspicious contribution, or a vulnerability in any code a contributor later adds — please report it.

Please report security, confidentiality, safety, or advice-boundary concerns using the [Safety Review issue template](.github/ISSUE_TEMPLATE/safety_review.yml) in this repository. Do not include confidential information, credentials, private documents, client data, employer data, principal information, or nonpublic investment details in any public issue.

Please include enough detail to reproduce or locate the concern. We aim to acknowledge reports promptly and address valid concerns in a reasonable timeframe.

## Responsible contribution

If you contribute to this repository, you must not introduce any of the following: confidential information; employer-, client-, or principal-specific data; real principal or family information; real investment, vendor, or counterparty data; confidential documents; live system details; live credentials; or executable code that connects to real systems without clear documentation and review. Contributions must not imply affiliation with or endorsement by any employer, client, principal, or named family office. See [CONTRIBUTING.md](CONTRIBUTING.md).
