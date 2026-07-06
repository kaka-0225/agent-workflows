---
description: Produce final structured AI infrastructure source-reading notes.
argument-hint: [repo-path] [optional-focus]
arguments: repo_path optional_focus
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# infra-summary

Produce final structured source-reading notes for an AI infrastructure
repository or feature.

## Execution Contract

You MUST base the summary on source files inside `$repo_path`.

You are forbidden from:

- Filling missing sections with guesses.
- Treating unverified performance hypotheses as facts.
- Creating output files without user confirmation.

## Workflow

1. Validate `$repo_path`.
2. Use `$optional_focus` when provided.
3. Invoke `infra-summary-agent`.
4. Apply `infra-summary-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the repository is missing or unreadable.

Mark uncertainty if major runtime paths, config effects, or backend behavior
cannot be verified from source.

## Output Summary

Return:

- Project or feature summary
- Architecture
- Execution path
- Core modules
- Config flow
- Tensor/KV cache flow
- Performance notes
- Evidence-backed facts
- Uncertain points
- Recommended next reading steps
