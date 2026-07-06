---
description: Understand one chapter or section of a book after reading.
argument-hint: [chapter-or-section]
arguments: chapter_or_section
allowed-tools:
  - Read
  - Agent
  - Skill
model: sonnet
---

# chapter-understand

Explain one chapter or section of a book using the provided text or accessible
book section.

## Execution Contract

You MUST base the explanation on `$chapter_or_section`.

You are forbidden from:

- Inventing chapter content.
- Mixing unrelated book content unless the user provides it.
- Treating interpretation as authorial fact.
- Diagnosing the reader or people described by the reader.

## Workflow

1. Validate `$chapter_or_section`.
2. Invoke `chapter-understanding-agent`.
3. Apply `chapter-understanding-template`.
4. Apply `evidence-checklist`.

## Failure Conditions

Stop if the section is missing or unreadable.

Mark uncertainty if the chapter is incomplete, OCR is unclear, or important
context is missing.

## Output Summary

Return:

- Chapter or section identity
- What the chapter is trying to do
- Key ideas
- Author viewpoint
- Agent explanation
- Important passages
- Possible misunderstandings
- Uncertain points
