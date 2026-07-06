# Placement Guide

Use this guide when copying or adapting `ai-infra-code-read`.

## Recommended Placement

For a source-reading workspace:

```text
workspace/
  ai-infra-code-read/
  source-project/
  docs/
    source-reading-notes/
```

For a project repository that should carry the workflow:

```text
project/
  AGENTS.md
  ai-infra-code-read/
  src/
  docs/
```

## Where Notes Should Go

Generated notes should usually go outside the raw source tree unless the user
confirms otherwise.

Recommended:

```text
docs/source-reading/
  codebase-map.md
  execution-trace.md
  kv-cache-map.md
  infra-summary.md
```

## What Not to Store Here

Do not store:

- Private repository credentials
- Benchmark results for unrelated projects
- Large generated logs
- Raw model weights or datasets
- Temporary scratch files

## Directory Creation Rule

Before creating workflow-specific output folders, propose the exact path and
wait for user confirmation.
