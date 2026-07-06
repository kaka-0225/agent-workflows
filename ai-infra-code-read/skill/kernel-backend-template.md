---
name: kernel-backend-template
description: Produce a standard kernel and backend dispatch map.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Kernel Backend Template

## Task

Map CUDA, Triton, attention backend, custom op, and dispatch logic.

## Expected Output

```md
# Kernel Backend Map

## Target

- Backend/feature:
- Repository:

## Dispatch Path

| Step | File | Symbol | Role | Evidence |
|---|---|---|---|---|

## Kernel or Custom Op Call Sites

| Call site | Kernel/op | Inputs | Outputs | Evidence |
|---|---|---|---|---|

## Shape/Dtype/Device Constraints

| Constraint | Location | Behavior |
|---|---|---|

## Fallback Paths

## Build or Extension Files

## External Dependencies

## Uncertain Points
```

## Rules

- Include fallback paths when found.
- Mark prebuilt binaries, external packages, and hardware-specific code as
  uncertainty when source is unavailable.
