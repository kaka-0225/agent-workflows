---
description: Build a structured map of one paper and recommend a reading path.
argument-hint: [paper-file]
arguments: paper_file
allowed-tools:
  - Read
  - Agent
  - Skill
model: haiku
---

# paper-map

Create a high-level map of one paper before deep reading.

## Execution Contract

You MUST use only the paper file provided as `$paper_file`.

You are forbidden from:

- Reading a different paper as a replacement.
- Inferring structure from filename alone.
- Performing multi-paper comparison.
- Modifying the original paper file.

## Workflow

1. Validate `$paper_file`.
2. Invoke `paper-structure-agent`.
3. Apply `paper-map-template`.
4. Return the paper map and recommended next command.

## Failure Conditions

Stop if the file is missing, unreadable, empty, or is a directory.

Mark uncertainty if section boundaries, figures, tables, or appendices cannot be
reliably parsed.

## Output Summary

Return:

- Paper identity
- Section/module map
- Main problem
- Suggested reading order
- Unreadable or uncertain parts
