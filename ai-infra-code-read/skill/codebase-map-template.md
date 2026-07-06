---
name: codebase-map-template
description: Produce a standard repository map for AI infrastructure source reading.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Codebase Map Template

## Task

Produce a structured map of one AI infrastructure repository.

## Expected Output

```md
# Codebase Map

## Repository Identity

- Path:
- Project type:
- Main language(s):
- Package/build system:

## Top-Level Structure

| Path | Purpose | Evidence |
|---|---|---|

## Probable Entrypoints

| Entrypoint | Runtime purpose | Evidence | Confidence |
|---|---|---|---|

## Core Runtime Modules

| Module | Responsibility | Why it matters |
|---|---|---|

## AI Infra Focus Areas

- Serving/request path:
- Scheduler/batching:
- Model runner:
- Attention/backend:
- KV cache:
- Config:
- Tests/examples:

## Recommended Reading Order

1.
2.
3.

## Uncertain Points
```

## Rules

- Use source evidence for every major claim.
- Mark uncertain entrypoints instead of presenting guesses as facts.
- Do not modify source files.
