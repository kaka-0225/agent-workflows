---
description: Reflect on one quote or short passage from a book.
argument-hint: [quote-or-short-passage]
arguments: quote_or_short_passage
allowed-tools:
  - Read
  - Agent
  - Skill
model: sonnet
---

# quote-reflection

Perform close reading and gentle reflection on one quote or short passage.

## Execution Contract

You MUST focus on `$quote_or_short_passage`.

You are forbidden from:

- Expanding the quote into unsupported book-wide claims.
- Rewriting the quote as advice without preserving nuance.
- Diagnosing the reader.
- Ignoring ambiguity.

## Workflow

1. Validate the quote or passage.
2. Invoke `quote-reflection-agent`.
3. Apply `quote-reflection-template`.
4. Apply `evidence-checklist`.

## Failure Conditions

Stop if the quote or passage is missing.

Mark uncertainty if translation, OCR, speaker, or context is unclear.

## Output Summary

Return:

- Quote or passage
- Literal meaning
- Possible deeper meaning
- Emotional or philosophical tension
- Relation to the chapter if known
- Reflection prompts
- Uncertain points
