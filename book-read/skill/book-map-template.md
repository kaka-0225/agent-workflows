---
name: book-map-template
description: Produce a standard map for one reflective book reading session.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Book Map Template

## Task

Produce a structured map of one book or reading session.

## Expected Output

```md
# Book Map

## Book Identity

- Title:
- Author:
- Edition/source if known:
- Available material:

## Structure

| Part/Chapter/Section | Visible title | Apparent focus | Evidence |
|---|---|---|---|

## Major Themes

| Theme | Where it appears | Evidence | Confidence |
|---|---|---|---|

## Suggested Reading Path

1.
2.
3.

## Commands to Use Next

## Uncertain or Unavailable Parts
```

## Rules

- Do not infer full book content from title or reputation.
- Mark missing table of contents, chapters, page numbers, or unreadable text.
