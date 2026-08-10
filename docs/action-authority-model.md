# Action Authority Model

How to decide what an AI-assisted workflow is allowed to do, and what has to be true before it does it.

Most guidance on this question stops at "read-only." That is a clean rule and a good starting position, but it is a proxy. What an office actually needs to protect is not the absence of writes. It is the guarantee that **no consequential change happens without a named human approving that specific change, and that the change is independently confirmed afterward.** Read-only guarantees that by removing the capability. This document guarantees it by controlling it.

The distinction matters because offices do give AI-assisted workflows write access in practice, whether or not their written policy admits it. A policy that describes a posture the office does not hold provides no protection. It is better to draw the line precisely and defend it.

> Nothing here makes AI-assisted writes safe. It describes the conditions under which an office might accept the risk deliberately rather than by drift. An office that is not prepared to implement the verification step should stay read-only.

---

## The five states

Every AI-assisted action sits in exactly one of these states. The states are ordered by consequence, and each one has different requirements.

| State | What happens | Effect on a system of record | What it requires |
|-------|--------------|------------------------------|------------------|
| **1. Read** | The AI observes information | None | Approved, scoped, least-privilege access |
| **2. Draft** | The AI produces an artifact in the workspace | None | Human review before the artifact is used |
| **3. Proposal** | The AI writes a *pending* object into the target system | Present but inert; invisible to downstream consumers; reversible by deletion | A rendered, human-readable form of exactly what would take effect |
| **4. Approved execution** | A named human approves a specific proposal and it takes effect | Real | Recorded approval identifying person, object, and time |
| **5. Verification** | An independent read confirms the change exists and is correct | Confirms or refutes state 4 | A read path different from the write path |

Two rules govern the sequence.

**A proposal is not an action.** State 3 is the safety mechanism that makes state 4 reviewable. An unposted journal entry, an unsent email draft, an unpublished record: these can be inspected, corrected, and deleted with no consequence. Systems that cannot represent a pending object cannot support this model, and workflows against them should stop at state 2.

**State 5 is mandatory, and its absence is a failure, not a neutral outcome.** An action that has been executed but not verified has an unknown status. It has not succeeded. Treating "no error was reported" as equivalent to "it worked" is the single most common way these workflows fail quietly, and it is the reason this document exists.

---

## Where the line falls: records versus resources

"Write" is too coarse a word to build a policy on. A journal entry records something that already happened. A wire transfer makes something happen. Both are writes. They are not remotely the same risk.

Draw the line at reversibility and reach:

**May be written, at state 4, with a named approver:**

- **Records of things that already occurred:** ledger entries, reconciliations, meeting notes, CRM activity, task status, document metadata. These describe history. They are correctable, auditable, and contained within the office.

**Never written by an AI-assisted workflow, regardless of approval:**

- **Movement of money or assets:** payments, wires, transfers, trades, subscriptions, redemptions.
- **External communication:** anything that leaves the office and cannot be recalled.
- **Contractual commitment:** signatures, acceptances, orders, engagement of counterparties.
- **Allocation and investment decisions:** what to buy, sell, hold, or weight.
- **Access, permission, and security state:** credentials, roles, sharing, retention, deletion.
- **Irreversible destruction:** hard deletes, purges, overwrites without recovery.

An AI-assisted workflow may prepare any of these for a person. A person performs them.

The test for anything not listed: *if this is wrong and nobody notices for thirty days, what is the cost, and can it be undone?* Contained and correctable belongs in the first group. Escaped or irreversible belongs in the second.

---

## What has to be true before an office operates at state 4

These are the conditions, not a maturity path. An office that cannot meet them should stay at state 2 or 3.

**Separation of proposer and approver.** The party that composes a change should not be the party that approves it. Where a lean office cannot separate the people, separate the moments: preparation and approval happen in distinct sessions, against source evidence, not against the AI's summary of the source evidence. A reviewer reading only the AI's own description of its work is not a control.

**The approved object is the executed object.** Record an immutable fingerprint of the proposal at approval, and confirm at execution that the fingerprint still matches. Without this, a proposal can change between review and execution and nobody would know.

**Verification through a different path.** Confirm the change through a report, export, or separate read interface, not through the response of the call that made it, and not through the same interface that wrote it. An interface that reported a change incorrectly will report it incorrectly again when asked to confirm its own work.

**Verification is classified, not binary.** The outcomes are: verified, absent despite reported success, present but altered, duplicated, and indeterminate. *Indeterminate is treated as failure.* A workflow that can only say "success" or "error" cannot detect the failures that matter.

**A tested reversal path.** Know how to unwind the change, and test it before the first real use, not during the first real incident.

**Scope limits that are enforced, not intended.** Least-privilege credentials, locked prior periods, batch size caps, value thresholds above which a second approver is required, and a way to disable execution immediately without deploying anything.

**Provenance on every artifact.** Source evidence, the proposal, the approver's identity, the timestamps, and the verification result stay linked. If you cannot reconstruct why a record exists six months later, the workflow is not auditable regardless of how it behaved.

**Source text is untrusted.** Transaction memos, vendor names, document contents, and imported descriptions are data, not instructions. They arrive from outside the office and can be authored by someone who wants the workflow to behave differently. Treat them accordingly.

---

## Why approval gates fail, and what to do about it

An approval gate is a control only if something enforces it. In practice they fail in recognizable ways, and an office should design against each one specifically.

**The gate was never read.** A workflow proceeds on a plan whose approval was recorded somewhere the workflow does not consult, such as a checkbox in a document or an agreement in conversation. *Control: the approval must be a machine-readable record that the workflow queries and hard-stops on. If a workflow can complete without reading the gate, there is no gate.*

**The gate was satisfied by the wrong object.** Approval was given for one item and applied to another, or to a batch that quietly grew after approval. *Control: approve specific fingerprinted objects, never categories or batches described in prose.*

**The gate passed and the action did not happen.** The system reported success, returned an identifier, and the change never reached the record. Everything downstream then treats the record as complete. *Control: state 5, through an independent path.*

**The gate passed and the action happened twice.** A retry, a resubmission, or a duplicate proposal produced two effects from one approval. *Control: idempotency keys, and duplicate detection as part of verification rather than as a later reconciliation problem.*

**The reviewer approved without the evidence.** Under time pressure, review degrades into acknowledgment. This is the failure mode that no amount of tooling prevents. *Control: make the review artifact show source evidence beside the proposed change, so approving without looking requires actively ignoring something rather than simply moving fast.*

**The gate held for months and then quietly stopped.** A configuration change, an expired credential, or a silent error turns enforcement off while the workflow keeps reporting normal operation. *Control: assert the gate's presence periodically as its own check, and alarm on the absence of expected approvals rather than only on their rejection.*

---

## Relationship to the rest of this library

Most workflows in this library operate at states 1 and 2, and should. They draft, summarize, and structure for a person. That is where the leverage is, and it carries the least risk.

States 3 through 5 apply where an office has chosen to connect a workflow to a system of record. This repository documents the pattern and the controls. It does not provide integrations, credentials, or executable code, and connecting a system remains the office's decision and responsibility.

See also: [AI Governance for Family Offices](ai-governance-for-family-offices.md), [Connectors and Context Access](connectors-and-context.md), [Skill Maturity Matrix](skill-maturity-matrix.md), and the [Threat Model](threat-model.md).

---

*This document is operational guidance, not legal, compliance, accounting, investment, or cybersecurity advice, and creates no professional or fiduciary relationship. The controls described are design patterns, not enforceable guarantees; an AI system may not follow instructions reliably, and a named human remains accountable for every change. Whether to grant an AI-assisted workflow any write access to a system of record is a governance decision that should involve the office's own professional advisers.*
