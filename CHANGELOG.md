# Changelog

All notable changes to this repository are documented here. This project follows
[Keep a Changelog](https://keepachangelog.com/) conventions and
[Semantic Versioning](https://semver.org/) where applicable.

## [Unreleased]

### Added

- **[Month-End Close](playbooks/month-end-close.md)** (`playbooks/`): the monthly
  operating rhythm, and the base the quarterly close now builds on. The library
  previously documented only a quarter-end close, which quietly implied that
  quarterly closing is the norm. Most lean offices close monthly, and an office
  that defers turns the quarter into an investigation rather than a review.

  Its thesis is that the monthly close is where an office either stays current
  or falls behind without being told. Queues get emptied rather than resolved.
  Transactions land in the month they were noticed rather than the month they
  occurred. Recurring entries keep posting after the arrangement behind them
  changed. Intercompany drifts because nobody ties it until quarter end. None of
  that raises an error, so the books look processed.

  Six review gates, including a **resolution gate** (an item cleared to empty a
  queue has not been resolved), an **intercompany gate** requiring each entity
  pair to tie both ways in the same session, and a **preparer and reviewer gate**
  requiring the review to run against source evidence rather than the preparer's
  own summary. Eight common failure points, each with its control.

  Composes the four ledger control skills and depends on written conventions;
  where those do not exist the routine escalates rather than infers. See
  [standing-context.md](docs/standing-context.md).

### Changed

- **[Quarter-End Close](playbooks/quarter-end-close.md)** now nests on the
  monthly cadence instead of running parallel to it. It states plainly that it
  does not repeat the transaction queues, account reconciliations, intercompany
  tie-out, or reviewer gate, and covers only what a quarter adds: lagged
  investment values, consolidation and elimination, the family reporting
  package, and the heavier independent review. Playbook count updated from ten
  to eleven.

### Added

- **[Standing Context](docs/standing-context.md)** (`docs/`) and
  **[accounting conventions template](templates/accounting-conventions-template.md)**
  (`templates/`): the substrate the skills depend on, which the repository
  previously assumed without naming.

  Skills in this library repeatedly defer outward. They say *retrieve the
  office's existing allocation policy rather than inventing one*, and they mark
  output *(missing)* when no chart of accounts, matching tolerance, or
  pending-item policy was provided. Those deferrals are deliberate, but they
  create a dependency: an office that runs a structured workflow with no written
  conventions gets *ask a person* on nearly every line and concludes the workflow
  does not work. It worked as designed. The layer underneath was missing.

  Distinguishes **run context** (what a workflow is given for one task, already
  covered by connector governance) from **standing context** (conventions,
  structure, decisions, and institutional memory, true across every run).
  Connecting more systems supplies the first and never the second.

  Covers the four categories, the minimum set the accounting routines actually
  reach for, ownership and maintenance including effective-dating and stated
  precedence, and how the substrate fails: conventions that live only in
  someone's head, a house convention mistaken for a general truth, records that
  capture intent instead of effect, summaries that go stale faster than the
  documents beneath them, and documents that disagree without either knowing.

  The closing method is the practical part: do not start by writing policy.
  Run a workflow, collect everything it returned as *(missing)*, and that list is
  the most accurate inventory of undocumented conventions an office is likely to
  get.

  Cross-referenced from the reference architecture's context layer, the
  connector guidance, and all four ledger control skills.

- **Ledger control workflows** (`skills/`): four accounting-control skills, made
  in scope by the action authority model. All are read-only and
  judgment-support: they analyze and draft, and a person records, reconciles,
  and signs.
  - **[Pre-Booking Gap Analysis](skills/pre-booking-gap-analysis/)**: establishes
    what a ledger already contains before entries are prepared. The default
    failure when AI assists with bookkeeping is additive, preparing entries
    because source activity exists without checking what is already recorded.
    Classifies every source item as already booked, partially booked, covered by
    an aggregate entry, pending, a duplicate representation, genuinely missing,
    or ambiguous, and drafts entries only for the genuinely missing population.
  - **[Post-Write Verification](skills/post-write-verification/)**: tests whether
    an approved change actually landed, comparing it field by field against
    evidence read back through a path different from the one that wrote it.
    Classifies each result as verified, absent, altered, duplicated, or
    indeterminate, and treats indeterminate as a failure. A success response or
    a returned identifier is never accepted as evidence of presence.

  - **[Transfer and Duplicate Review](skills/transfer-duplicate-review/)**: finds
    where one economic event has been represented more than once across
    accounts. Money moving between accounts the office controls is one event
    that arrives as several source rows. Distinguishes a duplicate source
    *representation* from an accounting *leg*, since one event still requires
    both a debit and a credit. Cross-entity movements are escalated rather than
    resolved: how a movement between legal entities is recorded follows the
    office's agreements and policy.
  - **[Reconciliation Evidence Pack](skills/reconciliation-evidence-pack/)**:
    assembles what a person needs to reconcile an account, testing completeness
    and validity as two separate assertions rather than producing one difference
    figure. Gross movements are always stated before any net, because a zero net
    difference can be produced by offsetting errors. Ledger-derived evidence is
    never treated as independent of the ledger, so a roll-forward of the ledger
    using ledger activity does not count as a second direction.

  No skill reconciles, books entries, eliminates intercompany items, or signs off
  a close, consistent with the [quarter-end close playbook](playbooks/quarter-end-close.md).

- **Evaluation examples** (`evals/`): non-executable red-team scenarios for
  [post-write verification](evals/post-write-verification-evals.md) (the system
  reports success with no evidence, the ghost entry, scope mistaken for absence,
  same-path verification presented as independent, and being asked to fix what
  was found) and for [transfer and duplicate review](evals/transfer-duplicate-review-evals.md)
  (the triple-count, same amount on consecutive days but unrelated, a
  cross-entity movement framed as cleanup, a confident conclusion from missing
  accounts, and an amount difference used to break a real pending-and-settled
  pair).

  Catalog entries added and validated against the manifest schema. Skill count
  updated from seven to eleven.

### Changed

- **Action authority replaces blanket read-only as the safety posture.** The repository
  previously described itself as read-only by default and stated that skills "never
  decide, transact, approve, or send." Read-only was a proxy: it guaranteed human
  accountability by removing capability rather than by controlling it. In practice
  offices do grant AI-assisted workflows write access to systems of record, and a
  written posture the office does not hold provides no protection. The requirement is
  now stated directly (**no consequential change without a named human approving that
  specific change, and independent verification that it landed**), and the boundary is
  drawn at **records versus resources** rather than at read versus write.

  What this does *not* change: nothing in this library sends external communication,
  moves money or assets, commits the office contractually, decides an allocation,
  alters access or permission state, or deletes irreversibly. Those remain prohibited
  with or without approval. Human review remains the primary control, guardrails
  remain instructions rather than enforceable controls, and the repository remains
  non-executable, credential-free, and free of shipped integrations.

  Updated accordingly: `README.md` (trust and safety posture), `CLAUDE.md` (repo
  purpose, identity, safety rules, prohibited content, review checklist),
  `ROADMAP.md` (current focus and out-of-scope list),
  `docs/skill-maturity-matrix.md`, `docs/ai-workforce-operating-model.md`,
  `docs/connectors-and-context.md`, and `.github/pull_request_template.md`.
  References to read-only *connector access* are unchanged; least-privilege retrieval
  of context is a separate matter from write authority, and remains the default.

### Added

- **[Action Authority Model](docs/action-authority-model.md)** (`docs/`): the five states
  an AI-assisted action can occupy (read, draft, proposal, approved execution,
  verification), the records-versus-resources boundary, the conditions an office must
  meet before operating at approved execution, and a catalogue of the ways approval
  gates fail silently in practice, including gates that are never read, gates
  satisfied by the wrong object, actions that report success without taking effect,
  and enforcement that lapses quietly after months of apparently normal operation.
  Read-only, human-in-the-loop, non-advisory, and non-executable, consistent with the
  rest of the repository.

- **Operating Playbooks** (`playbooks/`): a new top-level section documenting how
  recurring family office responsibilities are executed and where AI reduces
  administrative burden while human review stays the primary control. Includes a
  `README.md`, a `PLAYBOOK-TEMPLATE.md`, and ten playbooks: principal weekly
  review, capital call processing, investment opportunity intake, board and
  committee meeting preparation, executive travel coordination, insurance renewal
  management, vendor onboarding and review, quarter-end close, entity governance
  calendar, and document review for counsel. Each follows the same structure,
  separates AI assistance from human responsibility, contains explicit review
  gates, and cross-links the relevant skills, blueprints, case studies, and
  governance documents. Read-only, human-in-the-loop, non-advisory, and
  non-executable, consistent with the rest of the repository.
- Each playbook carries substantive family office operating detail: institutional
  controls such as segregation of duties, dual authorization, independent
  out-of-band verification, authorized-signer matrices, and recurring governance
  calendars: written so an experienced operator learns how the process is run
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
