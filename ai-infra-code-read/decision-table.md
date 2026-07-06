# ai-infra-code-read Decision Table

Use this table to decide which command, agent, or skill should be used.

| Need | Use |
|---|---|
| Understand a new AI infra repository | `codebase-map` |
| Find the path from an entrypoint to runtime logic | `execution-trace` |
| Read one file or module deeply | `module-read` |
| Understand how a config parameter works | `config-map` |
| Track tensor, token, batch, shape, dtype, or device flow | `tensor-flow` |
| Understand KV cache allocation, block tables, reuse, or quantization | `kv-cache-map` |
| Identify hot paths or possible bottlenecks | `performance-path` |
| Locate CUDA, Triton, attention backend, or dispatch logic | `kernel-map` |
| Produce final source-reading notes | `infra-summary` |
| Need source evidence and uncertainty checks | `evidence-checklist` |

## Default Flow

```text
codebase-map
execution-trace
module-read
config-map
tensor-flow
kv-cache-map
performance-path
kernel-map
infra-summary
```

Skip commands that are irrelevant to the target repository. For example, a
small pure-Python project may not need `kernel-map`, while a KV cache
quantization project may start with `kv-cache-map`.
