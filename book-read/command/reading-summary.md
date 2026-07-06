---
description: Produce staged or final structured notes for a book reading session.
argument-hint: [reading-material-or-notes]
arguments: reading_material_or_notes
allowed-tools:
  - Read
  - Agent
  - Skill
model: sonnet
---

# reading-summary

Produce staged or final reading notes from provided material or previous notes.

## Execution Contract

You MUST base the summary on `$reading_material_or_notes`.

You are forbidden from:

- Filling missing chapters with prior knowledge.
- Quoting excessive copyrighted text.
- Treating the summary as a replacement for `passage-read`.
- Creating output files without confirmation.

## Workflow

1. Validate `$reading_material_or_notes`.
2. Invoke `reading-summary-agent`.
3. Apply `reading-summary-template`.
4. Apply `evidence-checklist`.

## Failure Conditions

Stop if the provided material or notes are missing.

Mark uncertainty if notes are incomplete or passages are unavailable.

## Output Summary

Return:

- Reading scope
- Core ideas
- Important quotes or passages
- Personal takeaways if provided
- Open questions
- Re-read list
- Next reading action
