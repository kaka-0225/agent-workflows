---
description: Identify performance-critical paths and bottleneck hypotheses in AI infrastructure code.
argument-hint: [repo-path] [path-or-feature]
arguments: repo_path path_or_feature
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# performance-path

Analyze a performance-sensitive path and identify evidence-backed hot paths and
bottleneck hypotheses.

## Execution Contract

You MUST treat bottlenecks as hypotheses unless backed by profiling, benchmark
results, explicit comments, or strong source evidence.

You are forbidden from:

- Claiming measured performance without measurements.
- Running benchmarks or profiling commands without explicit user approval.
- Modifying code.
- Ignoring CPU/GPU synchronization, memory movement, batching, and kernel
  dispatch.

## Workflow

1. Validate inputs.
2. Locate the requested `$path_or_feature`.
3. Invoke `performance-analysis-agent`.
4. Apply `performance-path-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the target path cannot be located.

Mark uncertainty if performance depends on runtime workload, hardware, backend,
or external compiled code.

## Output Summary

Return:

- Target performance path
- Hot path candidates
- Latency and throughput factors
- Memory and synchronization concerns
- Kernel/backend concerns
- Bottleneck hypotheses
- Verification ideas
