# AI Infra Source Reading Rules

Use these rules when applying the `ai-infra-code-read` workflow.

## Language

- Default user-facing responses should be in Chinese.
- Keep source identifiers, paths, config keys, command names, and error messages
  in their original language.

## Evidence Discipline

- Do not invent architecture, call chains, tensor shapes, config effects, or
  performance behavior.
- Prefer evidence from source files, symbols, call sites, config definitions,
  tests, docs, and examples.
- Separate:
  - source facts
  - docs/comments
  - reasonable inference
  - performance hypothesis
  - uncertainty
  - needs-runtime-check

## Source Safety

- Do not modify source code unless the user explicitly asks for an
  implementation change.
- Do not run benchmarks, profilers, or expensive scripts without user approval.
- Do not create notes, output directories, or generated files without first
  discussing placement.

## AI Infra Priorities

When reading source code, prioritize:

- Entrypoints and public APIs
- Request, batch, scheduler, worker, model runner, and output paths
- Config definitions, defaults, overrides, and consumers
- Tensor/token/batch shape, dtype, device, and movement
- KV cache allocation, block table, reuse, eviction, quantization, and attention
  integration
- Attention backend dispatch, CUDA/Triton kernels, custom ops, and fallback
  paths
- Parallelism, communication, sharding, and memory pressure when present

## Performance Claims

- Treat bottlenecks as hypotheses unless backed by profiling, benchmark output,
  explicit comments, or strong source evidence.
- Say what measurement would confirm or disprove the hypothesis.
- Mark hardware-dependent, workload-dependent, and backend-dependent behavior as
  uncertainty.
