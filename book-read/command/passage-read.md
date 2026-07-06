---
description: Read provided passage literally and translate if needed, without summary or analysis.
argument-hint: [passage-or-file-section]
arguments: passage_or_file_section
allowed-tools:
  - Read
  - Agent
  - Skill
model: sonnet
---

# passage-read

Read the provided passage faithfully. Translate English passages into Chinese
when needed. Do not summarize, analyze, shorten, or expand.

## Execution Contract

You MUST preserve the content provided in `$passage_or_file_section`.

You are forbidden from:

- Summarizing.
- Analyzing.
- Explaining themes.
- Adding personal advice.
- Removing paragraphs or compressing meaning.
- Reconstructing missing book text from memory.

## Workflow

1. Validate the provided passage or file section.
2. Invoke `literal-reading-agent`.
3. Apply `passage-reading-template`.
4. Apply `evidence-checklist`.
5. Return original text and translation only.

## Failure Conditions

Stop if the passage or referenced file section is missing or unreadable.

Mark uncertainty if OCR, PDF extraction, page boundaries, or paragraph breaks
are unclear.

## Output Summary

Return:

- Source label
- Original text, preserving paragraph structure
- Chinese translation if needed
- OCR or extraction uncertainty
- No summary and no analysis
