---
name: passage-reading-template
description: Preserve provided text and translate English passages without summary or analysis.
user-invocable: true
allowed-tools:
  - "Read"
---

# Passage Reading Template

## Task

Read provided text faithfully and translate it when needed.

## Expected Output

```md
# Passage Read

## Source

- Book/chapter/page if known:
- Input type:
- Reading mode: literal reading and translation only

## Original Text

[Preserve the provided paragraph structure. Do not shorten.]

## Chinese Translation

[Translate paragraph by paragraph. Preserve paragraph order. Do not add
summary, analysis, or advice.]

## Unclear Text

- OCR/extraction uncertainty:
- Missing or cut-off text:
```

## Rules

- Do not summarize.
- Do not analyze.
- Do not shorten.
- Do not add interpretation or personal advice.
- Preserve paragraph structure when possible.
- If the original is already Chinese, return the original text and note that no
  translation is needed.
