# AGENTS.md

Guidance for Codex when working with the `ai-infra-code-read` workflow.

## Purpose

This workflow supports source reading for AI infrastructure projects, including
LLM serving engines, training systems, attention backends, KV cache projects,
kernel dispatch layers, and performance optimization code.

## Scope

This workflow supports:

- Repository structure mapping
- Runtime execution tracing
- Single-module or single-file reading
- Configuration flow analysis
- Tensor, token, batch, dtype, device, and shape tracing
- KV cache lifecycle analysis
- Performance-critical path analysis
- CUDA, Triton, attention backend, and kernel dispatch reading
- Final structured source-reading notes

This workflow does not support:

- Unrequested code modification
- General code review as the primary task
- Benchmarking or profiling without user confirmation
- Creating messy notes or output directories without placement discussion
- Making performance claims without evidence or uncertainty marking

## Language

- Default user-facing responses should be in Chinese.
- Keep code identifiers, file paths, command names, frontmatter fields, config
  keys, API names, and error messages in their original language.
- Follow explicit user requests for another output language.

## Working Rules

- Do not invent call chains, config effects, tensor shapes, or performance
  behavior.
- Prefer direct source evidence: file path, class name, function name, config
  key, call site, and data structure.
- Separate source facts, comments/docs, reasonable inference, and uncertainty.
- Before creating new directories or output files, propose the layout and get
  user confirmation.
- Do not edit source code unless the user explicitly asks to implement a
  change.
- When reading performance-sensitive code, avoid unsupported bottleneck claims.
  Mark bottlenecks as hypotheses unless backed by profiling, benchmarks, or
  explicit source comments.
- When a path cannot be traced completely, state where the trace stops and what
  evidence is missing.

## AI Infra Reading Priorities

Prioritize:

- Entrypoints and public APIs
- Request, batch, scheduler, worker, model runner, and output paths
- Config definitions, defaults, overrides, and runtime consumers
- Tensor/token/batch shape, dtype, device, and movement
- KV cache allocation, block table, reuse, eviction, quantization, and attention
  integration
- Attention backend dispatch, CUDA/Triton kernels, fallback paths, and shape
  constraints
- Parallelism, communication, sharding, and memory pressure when present

## Workflow Boundaries

- Commands coordinate workflow steps.
- Agents perform specialist source reading and analysis.
- Skills provide reusable templates and checklists.
- Rules protect source files and define workflow scope.

## Directory Rules

- `command/`: workflow entry points.
- `agent/`: specialist AI infra source-reading roles.
- `skill/`: reusable source-reading methods and output templates.
- `memory-rules/`: durable rules for this workflow.

## Verification

Before reporting completion, state:

- What repository, module, or path was read
- What source evidence was found
- What could not be verified
- What remains uncertain
- What next reading action is recommended
