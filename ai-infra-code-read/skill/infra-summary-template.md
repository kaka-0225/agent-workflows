---
name: infra-summary-template
description: Produce final structured AI infrastructure source-reading notes.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Infra Summary Template

## Task

Produce final structured notes for an AI infrastructure repository or feature.

## Expected Output

```md
# AI Infra Source Reading Summary

## Identity

- Repository/path:
- Feature/focus:
- Reading status:

## What This Codebase Does

## Architecture

## Main Execution Path

## Core Modules

| Module | Responsibility | Evidence |
|---|---|---|

## Config Flow

## Tensor/Data Flow

## KV Cache Flow

## Kernel/Backend Flow

## Performance Notes

## Evidence-Backed Facts

| Fact | Evidence | Confidence |
|---|---|---|

## Inferences and Hypotheses

| Inference/Hypothesis | Basis | How to verify |
|---|---|---|

## Uncertain Points

## Suggested Next Reading Actions
```

## Rules

- Do not fill missing sections with guesses.
- Separate facts, inferences, hypotheses, and uncertainty.
