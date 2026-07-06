---
description: Analyze KV cache lifecycle, block tables, reuse, quantization, and attention links.
argument-hint: [repo-path] [optional-topic]
arguments: repo_path optional_topic
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# kv-cache-map

Analyze KV cache design and lifecycle in an AI infrastructure codebase.

## Execution Contract

You MUST inspect KV cache related source files inside `$repo_path`.

Use `$optional_topic` to narrow the reading when provided, such as block table,
eviction, quantization, dtype, allocation, or attention integration.

You are forbidden from:

- Assuming the project uses a specific KV cache design without evidence.
- Claiming quantization or eviction support without locating implementation.
- Modifying source code.

## Workflow

1. Validate `$repo_path`.
2. Search for KV cache, block, page, cache manager, attention metadata, and
   quantization related symbols.
3. Invoke `kv-cache-agent`.
4. Apply `kv-cache-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the repository is missing or unreadable.

Mark uncertainty if KV cache behavior lives in external kernels or backend
libraries that are not available in source.

## Output Summary

Return:

- KV cache components
- Allocation and freeing path
- Block/page/table design
- Attention integration
- Quantization/dtype behavior
- Reuse/eviction behavior
- Evidence and uncertain points
