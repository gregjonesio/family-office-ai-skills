---
name: document-digest
description: Use this skill to summarize an administrative, legal, insurance, trust, entity, subscription, or operating document into plain-English notes. Produces a digest covering the document type, a plain-English summary, key parties, key dates, obligations, risks or unusual terms, questions for counsel or an advisor, and action items. It does not provide legal, tax, or accounting advice.
---

# Document Digest

## Purpose

This skill summarizes a dense administrative, legal, insurance, trust, entity, subscription, or operating document into clear, plain-English notes an operator can actually use. It identifies what the document is, what it says, who is involved, the key dates and obligations, and anything unusual — and it produces the questions to put to counsel or an advisor. It makes documents legible and surfaces what needs professional review. It is **not** a substitute for legal, tax, or accounting advice.

## When to use this

- Getting a plain-English read of a document before it goes to counsel or an advisor.
- Extracting the key dates and obligations from a contract, policy, or agreement.
- Triaging a stack of administrative or operating documents into usable notes.
- Building a digestible record of what a document contains for institutional memory.

## Inputs

Provide whatever you have; the skill works with excerpts and flags gaps.

- **The document** or a representative excerpt (administrative, legal, insurance, trust, entity, subscription, operating).
- **Document type** if known.
- **Why you are reviewing it** (the decision or task it relates to), if relevant.

## Output

Produce a digest with these sections, in this order:

1. **Document type** — what kind of document this is.
2. **Plain-English summary** — what it does and says, in accessible language.
3. **Key parties** — who is involved and their role.
4. **Key dates** — effective dates, deadlines, renewal/expiry, notice periods.
5. **Obligations** — what each party must do.
6. **Risks / unusual terms** — anything notable, one-sided, or atypical (flagged, not adjudicated).
7. **Questions for counsel or advisor** — what a professional should confirm or interpret.
8. **Action items** — concrete next steps for the operator.

## Instructions

- Summarize only what the document says. Do not infer terms that are not present, and do not fill gaps with general knowledge of how such documents "usually" read.
- Write the plain-English summary for an intelligent non-lawyer. Define legal or technical terms in passing.
- Extract **dates and obligations precisely.** If a date or notice period is ambiguous, flag it rather than guessing.
- Flag risks and unusual terms as **observations for professional review**, not as legal conclusions.
- Separate **what the document states** from **assumptions.** Mark inferred items *(assumption)*.
- Route anything requiring interpretation to *Questions for counsel or advisor*.
- Preserve confidentiality; treat the document as sensitive.

## Quality control

- **Missing information:** If the excerpt is partial or key sections are absent (e.g., termination, governing law, fees), say so explicitly rather than assuming standard terms.
- **Hallucination risk:** Do not invent clauses, dates, parties, or obligations. Legal documents must be summarized strictly from their text. Re-read and remove anything not supported by the document.
- **Confidentiality:** Treat the document as confidential. Introduce no outside information about the parties.
- **Uncertainty:** When the meaning of a clause is unclear, do not resolve it — flag it as a question for counsel.

## Do not

- Do not provide legal, tax, or accounting advice or interpret the document as a professional would.
- Do not state whether terms are enforceable, advisable, or sufficient.
- Do not invent clauses, dates, parties, or obligations.
- Do not assume "standard" terms that are not in the text.
- Do not recommend signing, declining, or executing the document.
- Do not omit the *Questions for counsel or advisor* section.

## Example request

> "Using the document-digest skill, summarize this document into plain-English notes and list questions for counsel: [paste document or excerpt]."

---

*This skill produces a plain-English summary to make a document legible and surface what needs professional review. It is not legal, tax, or accounting advice, does not interpret the document as a professional would, and does not recommend signing, declining, or executing it. Have qualified professionals review the full document before acting. A competent person must verify the summary against the source.*
