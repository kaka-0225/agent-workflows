---
description: Trace tensor, token, batch, shape, dtype, device, and data movement.
argument-hint: [repo-path] [symbol-or-path]
arguments: repo_path symbol_or_path
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# tensor-flow

Trace tensor, token, batch, shape, dtype, device, and data movement through a
selected runtime path.

## Execution Contract

You MUST focus on `$symbol_or_path` inside `$repo_path`.

You are forbidden from:

- Inventing tensor shapes, dtypes, or devices.
- Treating comments as guaranteed runtime behavior.
- Ignoring copy, slice, reshape, cast, or device transfer operations.

## Workflow

1. Validate inputs.
2. Locate relevant tensor-producing and tensor-consuming code.
3. Invoke `tensor-flow-agent`.
4. Apply `tensor-flow-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the target cannot be located or read.

Mark uncertainty if shapes depend on runtime values, backend-specific kernels,
or external compiled code.

## Output Summary

Return:

- Target tensor/data path
- Variables and data structures
- Shape/dtype/device evidence
- Transformations
- Copies and device movement
- Consumers
- Uncertain points
