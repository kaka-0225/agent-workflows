---
name: module-reading-template
description: Produce a standard deep reading note for one AI infrastructure module.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Module Reading Template

## Task

Read one file or module in depth.

## Expected Output

```md
# Module Reading

## Module Identity

- Path:
- Language:
- Module type:

## Responsibility

## Key Classes and Functions

| Symbol | Responsibility | Inputs | Outputs | Evidence |
|---|---|---|---|---|

## Important Data Structures

| Name | Role | Lifecycle |
|---|---|---|

## Dependencies

| Dependency | Used for | Evidence |
|---|---|---|

## Callers and Callees

| Direction | File/Symbol | Relationship |
|---|---|---|

## AI Infra Relevance

- Scheduler/batching:
- Model execution:
- KV cache:
- Attention/backend:
- Config:
- Performance:

## Risk or Complexity Points

## Uncertain Points
```

## Rules

- Stay focused on the requested module.
- Inspect nearby files only when needed to explain the module correctly.
