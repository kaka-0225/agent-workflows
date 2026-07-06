---
name: config-map-template
description: Produce a standard config flow map for AI infrastructure code.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Config Map Template

## Task

Trace a configuration key or topic from definition to runtime effect.

## Expected Output

```md
# Config Map

## Config Target

- Key/topic:
- Repository:

## Definition and Defaults

| File | Symbol/key | Default | Validation | Evidence |
|---|---|---|---|---|

## Override Paths

| Mechanism | Location | Notes |
|---|---|---|

## Runtime Consumers

| Consumer | File | Effect | Evidence |
|---|---|---|---|

## Behavioral Effect

## Related Configs

## Uncertain Points
```

## Rules

- Do not assume defaults.
- A config effect is not confirmed until at least one consumer is located.
