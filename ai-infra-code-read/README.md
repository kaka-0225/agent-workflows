# ai-infra-code-read

AI infrastructure source-reading workflow for Codex and Claude Code.

This workflow is designed for reading performance-sensitive AI systems code,
such as LLM serving engines, training infrastructure, KV cache projects,
attention backends, kernel dispatch layers, and multimodal model optimization
code.

It focuses on source understanding, not code modification. Use it to build a
verifiable map of architecture, execution flow, configuration flow, tensor
flow, KV cache behavior, and performance-critical paths.

## Recommended Reading Flow

1. `codebase-map`: build a map of the repository and recommended reading path.
2. `execution-trace`: trace one runtime path from entrypoint to core logic.
3. `module-read`: read one file or module in depth.
4. `config-map`: trace important configuration parameters.
5. `tensor-flow`: trace tensor, token, batch, dtype, device, and shape flow.
6. `kv-cache-map`: analyze KV cache allocation, reuse, eviction, and attention
   integration.
7. `performance-path`: identify performance-critical paths and bottleneck
   hypotheses.
8. `kernel-map`: locate CUDA, Triton, attention backend, and dispatch logic.
9. `infra-summary`: produce final structured source-reading notes.

## Commands

| Command | Purpose |
|---|---|
| `codebase-map` | Build repository map, core modules, entrypoints, and reading order. |
| `execution-trace` | Trace execution from an entrypoint through core runtime logic. |
| `module-read` | Read one module or file with caller/callee and responsibility analysis. |
| `config-map` | Trace config definitions, defaults, overrides, and runtime effects. |
| `tensor-flow` | Track tensor/token/batch shape, dtype, device, and data movement. |
| `kv-cache-map` | Analyze KV cache lifecycle, block table, quantization, and attention links. |
| `performance-path` | Analyze hot paths, latency/throughput factors, and bottleneck hypotheses. |
| `kernel-map` | Locate kernel/backend dispatch, CUDA/Triton calls, and fallback paths. |
| `infra-summary` | Produce final structured notes and uncertainty report. |

## Agents

| Agent | Purpose |
|---|---|
| `codebase-structure-agent` | Identifies repository structure, entrypoints, and core modules. |
| `execution-trace-agent` | Follows runtime call chains and state transitions. |
| `module-reader-agent` | Reads one file or module in depth. |
| `config-analysis-agent` | Tracks configuration parameters and their runtime effects. |
| `tensor-flow-agent` | Tracks tensor, token, batch, dtype, device, and shape flow. |
| `kv-cache-agent` | Analyzes KV cache design and lifecycle. |
| `performance-analysis-agent` | Reviews performance-critical code paths and bottleneck hypotheses. |
| `kernel-backend-agent` | Reads kernel, backend, attention, and dispatch layers. |
| `infra-summary-agent` | Synthesizes final source-reading notes. |

## Skills

| Skill | Purpose |
|---|---|
| `codebase-map-template` | Standard repository map output. |
| `execution-trace-template` | Standard execution trace output. |
| `module-reading-template` | Standard module reading output. |
| `config-map-template` | Standard config tracing output. |
| `tensor-flow-template` | Standard tensor/dataflow tracing output. |
| `kv-cache-template` | Standard KV cache analysis output. |
| `performance-path-template` | Standard performance path analysis output. |
| `kernel-backend-template` | Standard kernel/backend analysis output. |
| `infra-summary-template` | Final structured source-reading summary. |
| `evidence-checklist` | Source evidence and uncertainty check. |

## Non-Goals

- Do not modify source code unless the user explicitly switches to an
  implementation workflow.
- Do not benchmark or profile unless the user explicitly asks and approves the
  commands.
- Do not infer runtime behavior without code evidence or clear uncertainty.
- Do not create project notes or output files before confirming placement.
- Do not turn this workflow into a generic code-review workflow.
