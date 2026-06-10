# Rules Template

Use this template for path-scoped rules.

```md
---
paths:
  - "path-or-glob/**"
---

# Rule Name

## Purpose

Explain when this rule applies.

## Rules

- ...
- ...

## Routing

If work in this path requires a specialist agent, delegate to:

```text
Agent(subagent_type="...", description="...", prompt="...")
```

## Failure Conditions

- ...
```
