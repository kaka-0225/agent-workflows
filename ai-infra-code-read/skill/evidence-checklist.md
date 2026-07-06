---
name: evidence-checklist
description: Check source evidence, inference, and uncertainty in AI infrastructure source reading.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Evidence Checklist

## Task

Audit source-reading output for evidence quality.

## Checklist

Before finalizing, verify:

- Every architecture claim has a file path or symbol reference.
- Every call-chain step has caller/callee evidence or is marked uncertain.
- Every config default has source evidence or is marked not found.
- Every tensor shape, dtype, or device claim has source evidence or is marked
  runtime-dependent.
- Every KV cache behavior claim has implementation evidence or is marked
  uncertain.
- Every performance bottleneck is phrased as a hypothesis unless backed by
  measurements or explicit source comments.
- External dependencies, compiled kernels, dynamic dispatch, and runtime
  registration are marked as possible uncertainty sources.

## Evidence Labels

Use these labels:

- `source`: directly found in source code.
- `docs`: found in docs, comments, or examples.
- `inference`: reasonable inference from source context.
- `hypothesis`: plausible performance or behavior hypothesis.
- `uncertain`: not enough evidence.
- `needs-runtime-check`: requires execution, profiling, or benchmark.

## Rules

- Do not hide uncertainty.
- Do not upgrade inference into fact.
- Keep evidence concise and traceable.
