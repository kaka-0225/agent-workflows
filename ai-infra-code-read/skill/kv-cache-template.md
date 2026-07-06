---
name: kv-cache-template
description: Produce a standard KV cache analysis note for LLM infrastructure code.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# KV Cache Template

## Task

Analyze KV cache design and lifecycle.

## Expected Output

```md
# KV Cache Map

## Components

| Component | Role | File | Evidence |
|---|---|---|---|

## Lifecycle

| Stage | Operation | File/Symbol | Evidence |
|---|---|---|---|
| Allocate | | | |
| Write/update | | | |
| Read/use | | | |
| Reuse | | | |
| Free/evict | | | |

## Block/Page/Table Design

## Attention Integration

## Dtype and Quantization

## Scheduler/Batch Interaction

## Memory Management Notes

## Uncertain Points
```

## Rules

- Do not assume PagedAttention, block tables, eviction, or quantization exists.
- Mark external kernels or backend libraries as uncertainty when source is not
  available.
