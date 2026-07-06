---
description: Trace an AI infrastructure execution path from entrypoint to core logic.
argument-hint: [repo-path] [entrypoint-or-feature]
arguments: repo_path entrypoint_or_feature
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# execution-trace

Trace one runtime execution path through an AI infrastructure codebase.

## Execution Contract

You MUST trace only the requested `$entrypoint_or_feature` inside `$repo_path`.

You are forbidden from:

- Inventing callers or callees.
- Treating similarly named functions as connected without evidence.
- Modifying source code.
- Claiming runtime order without source evidence or uncertainty.

## Workflow

1. Validate `$repo_path` and `$entrypoint_or_feature`.
2. Locate likely entrypoint files and symbols.
3. Invoke `execution-trace-agent`.
4. Apply `execution-trace-template`.
5. Apply `evidence-checklist`.
6. Return the trace and any gaps.

## Failure Conditions

Stop if the repository or target cannot be read.

Mark uncertainty if dynamic dispatch, decorators, config-driven selection, or
runtime registration prevents a complete static trace.

## Output Summary

Return:

- Requested path
- Entrypoint
- Step-by-step call chain
- Key state transitions
- Important data structures
- Evidence locations
- Trace gaps and next files to inspect
