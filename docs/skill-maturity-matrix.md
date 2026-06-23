# From Prompts to Operating Systems: Skill Maturity Matrix

How AI usage in a family office evolves — from a one-off prompt to a governed operating layer. The progression is about **structure, review, governance, measurement, and repeatability**, not autonomy. A more mature stage is more *reliable and reviewable*, not more independent. At every stage, a human remains accountable and the work stays read-only and non-advisory.

Use this matrix to locate where a given workflow sits today and what it would take to advance it deliberately.

---

## The matrix

| Stage | Description | Example | Benefits | Risks | Required to advance |
|-------|-------------|---------|----------|-------|---------------------|
| **0 — One-off prompt** | A single, ad hoc instruction to a model | "Summarize these meeting notes." | Fast; zero setup | Inconsistent; no rules; easy to misuse on sensitive data | Capture a reusable structure |
| **1 — Reusable template** | A fixed structure for an artifact, filled in each time | The [action item template](../templates/action-item-template.md) for meeting outputs | Consistent format; shareable | Structure without behavioral rules; quality varies | Add inputs, rules, quality control, and prohibitions |
| **2 — Skill** | A workflow contract: inputs, output, instructions, quality control, prohibitions | [Meeting Prep Pack](../skills/meeting-prep-pack/) | Predictable, reviewable output; explicit limits | Guardrails are instructions, not controls; still needs review | Run it as a repeatable, reviewed process |
| **3 — Workflow** | A skill run the same way every time, with a defined review gate | [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) run after every meeting, reviewed before use | Repeatable; review built in; less ad hoc risk | Review can slip under pressure; context may be incomplete | Combine skills + context + review + measurement |
| **4 — System** | Multiple skills, context sources, and review gates composed for an end-to-end outcome | A weekly briefing system using [Principal Weekly Brief](../skills/principal-weekly-brief/) + [Meeting Prep Pack](../skills/meeting-prep-pack/) + [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) (see [blueprints](../blueprints/)) | End-to-end leverage; consistent across a process | More moving parts; broader context/permission risk | Add governance, measurement, and a maturity/review cadence |
| **5 — Operating layer** | Systems running across functions under governance, measurement, and institutional memory | The [reference architecture](reference-architecture.md) realized across briefings, deal review, meetings, and vendors | Office-wide repeatability and institutional memory | Over-confidence at scale; autonomy creep; governance treated as "done" | Sustain it — review governance on a cadence; hold the human-in-the-loop line |

## Worked example: one task, five stages

Take meeting follow-through — a single recurring task — and watch it mature:

- **Stage 0.** Someone pastes raw notes and asks for a summary. Useful once.
- **Stage 1.** The office adopts the [action item template](../templates/action-item-template.md) so every summary has the same shape.
- **Stage 2.** It becomes the [Post-Meeting Action Extractor](../skills/post-meeting-action-extractor/) skill — with rules to flag missing owners/deadlines and to never auto-send.
- **Stage 3.** It runs after every meeting, with a named reviewer confirming owners before the action list is used.
- **Stage 4.** It joins [Meeting Prep Pack](../skills/meeting-prep-pack/) and [Principal Weekly Brief](../skills/principal-weekly-brief/) in a [meeting-to-execution system](../blueprints/meeting-to-execution-system.md).
- **Stage 5.** That system runs alongside others under shared governance and measurement, feeding institutional memory.

Notice what did **not** change across the stages: the AI never gained authority to send, decide, or commit. What improved was structure, consistency, review, and memory.

## The principle

> Higher maturity does not mean more autonomy. It means better structure, review, governance, measurement, and repeatability.

A common and dangerous misreading is that "advanced" AI use means handing the model more independence. The opposite is true here: the more mature the stage, the *more* deliberate the controls around it. Maturity is earned with governance, not with autonomy.

---

*This matrix is operational guidance, not legal, compliance, investment, or regulatory advice. Advancing a workflow is a governance decision, not just a technical one.*
