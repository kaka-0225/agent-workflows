---
name: execution-trace-template
description: Produce a standard execution trace for AI infrastructure code.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Execution Trace Template

## Task

Trace one runtime path from entrypoint to core logic.

## Expected Output

```md
# Execution Trace

## Requested Path

- Repository:
- Entrypoint or feature:
- Trace status:

## Entrypoint

- File:
- Symbol:
- Evidence:

## Call Chain

| Step | File | Symbol | Role | Evidence | Confidence |
|---|---|---|---|---|---|

## State Transitions

| State/Data | Before | After | Code location |
|---|---|---|---|

## Key Data Structures

| Data structure | Role | Where created | Where consumed |
|---|---|---|---|

## Dynamic Dispatch or Runtime Gaps

## Next Files to Inspect
```

## Rules

- Do not invent callers or callees.
- Mark dynamic dispatch, plugin registration, config selection, and external
  backend calls as uncertainty when static evidence is incomplete.
