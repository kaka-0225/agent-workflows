---
description: Locate kernel, backend, attention, CUDA, Triton, and dispatch logic.
argument-hint: [repo-path] [backend-or-feature]
arguments: repo_path backend_or_feature
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# kernel-map

Map kernel and backend dispatch logic for an AI infrastructure feature.

## Execution Contract

You MUST focus on `$backend_or_feature` inside `$repo_path`.

You are forbidden from:

- Assuming CUDA/Triton/FlashAttention behavior without source evidence.
- Ignoring fallback paths.
- Claiming kernel constraints without locating checks, signatures, or call
  sites.
- Modifying kernel code.

## Workflow

1. Validate inputs.
2. Search for backend registration, dispatch, kernel wrappers, custom ops,
   Triton kernels, CUDA extensions, and attention backends.
3. Invoke `kernel-backend-agent`.
4. Apply `kernel-backend-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the target backend or feature cannot be located.

Mark uncertainty if implementation is in prebuilt binaries, external packages,
or hardware-specific code not present in the repository.

## Output Summary

Return:

- Backend or feature
- Dispatch path
- Kernel call sites
- Shape/dtype/device constraints
- Fallback paths
- Build or extension files
- Uncertain points
