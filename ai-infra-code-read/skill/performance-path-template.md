---
name: performance-path-template
description: Produce a standard source-level performance path analysis.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Performance Path Template

## Task

Identify performance-critical paths and bottleneck hypotheses from source code.

## Expected Output

```md
# Performance Path

## Target

- Path/feature:
- Runtime context:

## Hot Path Candidates

| Candidate | Why it may be hot | Evidence | Confidence |
|---|---|---|---|

## Latency Factors

## Throughput Factors

## Memory and Synchronization Concerns

| Concern | Evidence | Why it matters |
|---|---|---|

## Kernel/Backend Concerns

## Bottleneck Hypotheses

| Hypothesis | Evidence | How to verify |
|---|---|---|

## Required Measurements

## Uncertain Points
```

## Rules

- Do not claim measured performance unless measurements are provided.
- Phrase bottlenecks as hypotheses unless directly proven.
