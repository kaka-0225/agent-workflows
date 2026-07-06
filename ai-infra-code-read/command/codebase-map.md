---
description: Build a structured map of an AI infrastructure repository.
argument-hint: [repo-path]
arguments: repo_path
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: haiku
---

# codebase-map

Create a high-level map of an AI infrastructure codebase before deep reading.

## Execution Contract

You MUST use only the repository path provided as `$repo_path`.

You are forbidden from:

- Reading an unrelated repository as a replacement.
- Inferring architecture from repository name alone.
- Modifying source files.
- Creating output files without user confirmation.

## Workflow

1. Validate `$repo_path`.
2. Inspect top-level directories, docs, examples, tests, and config files.
3. Invoke `codebase-structure-agent`.
4. Apply `codebase-map-template`.
5. Return the repository map and recommended next command.

## Failure Conditions

Stop if the path is missing, unreadable, empty, or is not a directory.

Mark uncertainty if entrypoints, runtime paths, or core modules cannot be
identified from available files.

## Output Summary

Return:

- Repository identity
- Top-level structure
- Probable entrypoints
- Core runtime modules
- AI infra focus areas
- Suggested reading order
- Uncertain or unreadable parts
