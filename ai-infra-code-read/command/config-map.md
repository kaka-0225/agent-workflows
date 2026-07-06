---
description: Trace configuration definitions, defaults, overrides, and runtime effects.
argument-hint: [repo-path] [config-key-or-topic]
arguments: repo_path config_key_or_topic
allowed-tools:
  - Read
  - Glob
  - Grep
  - Agent
  - Skill
model: sonnet
---

# config-map

Trace how one configuration key or topic is defined, parsed, overridden, and
used at runtime.

## Execution Contract

You MUST trace `$config_key_or_topic` inside `$repo_path`.

You are forbidden from:

- Assuming defaults without source evidence.
- Claiming runtime effects without locating consumers.
- Modifying config files.

## Workflow

1. Validate inputs.
2. Search for config definitions, defaults, CLI flags, env vars, dataclasses,
   schemas, and runtime consumers.
3. Invoke `config-analysis-agent`.
4. Apply `config-map-template`.
5. Apply `evidence-checklist`.

## Failure Conditions

Stop if the repository is missing or unreadable.

Mark uncertainty if config values are produced dynamically or depend on external
runtime state.

## Output Summary

Return:

- Config key/topic
- Definition location
- Default value if found
- Override mechanisms
- Runtime consumers
- Behavioral effect
- Uncertain points
