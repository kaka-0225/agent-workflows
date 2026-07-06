---
name: evidence-checklist
description: Check evidence, translation boundaries, and interpretation boundaries in book reading.
user-invocable: true
allowed-tools:
  - "Read"
---

# Evidence Checklist

## Task

Audit book-reading output for evidence, translation, and interpretation
boundaries.

## Checklist

Before finalizing, verify:

- `passage-read` contains no summary, analysis, advice, or theme extraction.
- Original text and translation are clearly separated.
- Author viewpoint and agent explanation are clearly separated.
- User reflection is not presented as fact.
- Unread or unavailable book content is not invented.
- OCR, extraction, missing page, or missing chapter uncertainty is marked.
- Sensitive topics are handled without diagnosis or judgment.
- Quotes from copyrighted books are kept brief unless the user provided the
  passage and requested transformation of that provided text.

## Evidence Labels

Use these labels:

- `provided-text`: directly provided by the user or file.
- `translation`: translation of provided text.
- `author-viewpoint`: the author's apparent claim from provided material.
- `agent-explanation`: explanatory interpretation by the agent.
- `user-reflection`: the user's own context or reflection.
- `uncertain`: not enough evidence.

## Rules

- Do not hide uncertainty.
- Do not turn interpretation into authorial fact.
- Do not turn reflection into diagnosis.
