---
description: Produce a final structured summary of one paper with evidence and uncertainty checks.
argument-hint: [paper-file]
arguments: paper_file
allowed-tools:
  - Read
  - Agent
  - Skill
model: haiku
---

# paper-summary

Produce a final structured reading note for one paper.

## Execution Contract

You MUST summarize only the provided paper.

You are forbidden from:

- Inventing missing information.
- Summarizing from title, abstract, filename, or prior knowledge only.
- Omitting uncertainty from unsupported or ambiguous claims.
- Comparing with other papers unless the user explicitly asks for a separate
  comparison workflow.

## Workflow

1. Validate `$paper_file`.
2. Invoke `literature-review-agent`.
3. Apply `paper-summary-template`.
4. Invoke `claim-audit-agent`.
5. Apply `claim-evidence-checklist`.
6. Return final notes.

## Failure Conditions

Stop if the file cannot be read or extracted text is clearly incomplete.

Mark uncertainty if sections, figures, tables, formulas, datasets, metrics, or
results cannot be verified from the paper.

## Output Summary

Return:

- Final structured notes
- Evidence-backed claims
- Weak or unsupported claims
- Unreadable sections or artifacts
- Suggested next reading action
