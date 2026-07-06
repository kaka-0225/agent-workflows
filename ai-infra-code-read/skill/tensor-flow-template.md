---
name: tensor-flow-template
description: Produce a standard tensor and dataflow trace for AI infrastructure code.
user-invocable: true
allowed-tools:
  - "Read"
  - "Glob"
  - "Grep"
---

# Tensor Flow Template

## Task

Track tensor, token, batch, shape, dtype, device, and movement through source
code.

## Expected Output

```md
# Tensor Flow

## Target

- Symbol/path:
- Runtime context:

## Flow Table

| Step | Variable/Data | Shape | Dtype | Device | Operation | Evidence |
|---|---|---|---|---|---|---|

## Producers

| Producer | Output | Evidence |
|---|---|---|

## Consumers

| Consumer | Input | Evidence |
|---|---|---|

## Transformations

- Reshape/view:
- Cast:
- Slice/index:
- Copy:
- Device transfer:
- Contiguity/layout:

## Runtime-Dependent Values

## Uncertain Points
```

## Rules

- If shape, dtype, or device is not explicit, write "not found in source".
- Separate source evidence from inference based on naming or context.
