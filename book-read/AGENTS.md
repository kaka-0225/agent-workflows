# AGENTS.md

Guidance for Codex when working with the `book-read` workflow.

## Purpose

This workflow supports careful reading of literature, psychology,
relationships, philosophy, and personal-growth books. It helps preserve text,
translate English passages, understand chapters, analyze themes, reflect on
quotes, guide personal reflection, and produce structured reading notes.

## Scope

This workflow supports:

- One book or one reading session at a time
- Passage-level literal reading and translation
- Chapter or section understanding
- Theme analysis using provided book evidence
- Quote and passage reflection
- Personal reflection connected to the reader's experience
- Staged or final reading summaries

This workflow does not support:

- Reconstructing books that were not provided
- Summarizing or analyzing inside `passage-read`
- Psychological diagnosis
- Presenting book claims as universal truth
- Creating output folders or notes without placement discussion

## Language

- Default user-facing responses should be in Chinese.
- Keep book titles, author names, chapter titles, quoted text, technical terms,
  and file paths in their original language when useful.
- For English passages, provide faithful and natural Chinese translation when
  requested by `passage-read`.
- Follow explicit user requests for another output language.

## Reading Boundaries

- `passage-read` is for original text preservation and translation only.
- `chapter-understand`, `theme-analysis`, `quote-reflection`,
  `personal-reflection`, and `reading-summary` may summarize, analyze, or
  reflect.
- Keep original text, translation, author viewpoint, agent explanation, and user
  reflection clearly separated.

## Working Rules

- Do not invent book content.
- Do not summarize from title, reputation, or prior knowledge only.
- When a passage, page, chapter, or section is unreadable, mark uncertainty.
- For OCR or PDF extraction errors, preserve the uncertainty instead of silently
  correcting meaning.
- Avoid judgmental, prescriptive, or diagnostic language.
- Treat sensitive topics such as intimacy, shame, self-worth, conflict, desire,
  anger, and relationships with respect and clear boundaries.
- Before creating new directories or output files, propose the layout and get
  user confirmation.

## Workflow Boundaries

- Commands coordinate workflow steps.
- Agents perform specialist reading, translation, analysis, or reflection.
- Skills provide reusable templates and checklists.
- Rules protect source material, interpretation boundaries, and note placement.

## Directory Rules

- `command/`: workflow entry points.
- `agent/`: specialist book-reading roles.
- `skill/`: reusable reading, translation, analysis, and reflection templates.
- `memory-rules/`: durable rules for this workflow.

## Verification

Before reporting completion, state:

- What book, chapter, passage, or theme was handled
- Whether the output is translation, explanation, analysis, or reflection
- What evidence or provided text was used
- What could not be verified
- What remains uncertain
