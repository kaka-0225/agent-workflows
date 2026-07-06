---
description: Build a map of one book, its structure, themes, and reading path.
argument-hint: [book-file-or-context]
arguments: book_file_or_context
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: haiku
---

# book-map

Create a high-level map of one book or reading session before deep reading.

## Execution Contract

You MUST use only the book file, chapter list, or context provided as
`$book_file_or_context`.

You are forbidden from:

- Reconstructing a book from memory.
- Inferring full content from title, reputation, or prior knowledge.
- Performing multi-book comparison unless the user explicitly asks.
- Modifying the original book file.

## Workflow

1. Validate `$book_file_or_context`.
2. Invoke `book-structure-agent`.
3. Apply `book-map-template`.
4. Return the book map and recommended next command.

## Failure Conditions

Stop if the file or context is missing, unreadable, empty, or unavailable.

Mark uncertainty if the table of contents, chapters, sections, or page
boundaries cannot be reliably parsed.

## Output Summary

Return:

- Book identity
- Available structure
- Major themes
- Suggested reading order
- Recommended next command
- Unreadable or uncertain parts
