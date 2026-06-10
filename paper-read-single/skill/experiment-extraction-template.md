---
name: experiment-extraction-template
description: Extract datasets, metrics, baselines, results, ablations, and evidence from one paper.
user-invocable: true
allowed-tools:
  - "Read"
---

# Experiment Extraction Template

## Task

Extract and evaluate experiment information from one paper.

## Expected Output

```md
# Experiment Analysis

## Datasets

| Dataset | Purpose | Evidence |
|---|---|---|

## Metrics

| Metric | Meaning | Evidence |
|---|---|---|

## Baselines

## Main Results

## Ablations

## Implementation Details

## Claim Support

| Claim | Supporting Experiment | Strength | Notes |
|---|---|---|---|

## Uncertain Or Unreadable Evidence
```

## Rules

- Do not invent numbers, baselines, datasets, or metrics.
- Mark unreadable tables and figures clearly.
