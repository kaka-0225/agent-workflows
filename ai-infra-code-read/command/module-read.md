---
description: Read one AI infrastructure module or file in depth.
argument-hint: [file-or-module-path]
arguments: module_path
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# module-read

Read one file or module and explain its role in the AI infrastructure system.

## Execution Contract

You MUST focus on `$module_path`.

You may inspect nearby imports, callers, callees, and tests only when needed to
explain the module accurately.

You are forbidden from:

- Expanding into a whole-repository review.
- Modifying the module.
- Explaining behavior without checking source evidence.

## Workflow

1. Validate `$module_path`.
2. Identify public classes, functions, data structures, and side effects.
3. Invoke `module-reader-agent`.
4. Apply `module-reading-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the module is missing, unreadable, or generated/binary content.

Mark uncertainty if important behavior depends on external compiled code,
runtime registration, or optional dependencies that are not available.

## Output Summary

Return:

- Module responsibility
- Key classes/functions
- Inputs and outputs
- Important dependencies
- Callers and callees
- AI infra relevance
- Uncertain points
