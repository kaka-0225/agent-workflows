---
name: claim-evidence-checklist
description: Check whether important paper claims are supported by evidence in the provided paper.
user-invocable: true
allowed-tools:
  - "Read"
---

# Claim Evidence Checklist

## Task

Audit important claims against the provided paper.

## Classification

- Supported: direct evidence exists in the paper.
- Weak: indirect or incomplete evidence exists.
- Unsupported: no evidence found in the provided text.
- Uncertain: extraction quality prevents reliable judgment.

## Expected Output

```md
# Claim Evidence Audit

| Claim | Evidence | Classification | Confidence | Notes |
|---|---|---|---|---|

## Unsupported Or Risky Claims

## Missing Evidence

## Extraction Limitations
```

## Rules

- Do not use outside knowledge as evidence.
- Do not upgrade weak evidence to supported.
- Mark unreadable tables, figures, formulas, or sections.
