# Command Template

Use this template for repeated workflows.

```md
---
description: One clear sentence describing what this command does.
argument-hint: [required-input]
arguments: required_input
allowed-tools:
  - AskUserQuestion
  - Agent
  - Skill
model: haiku
---

# Command Name

Short purpose statement.

## Execution Contract

You MUST ...

You are forbidden from:
- ...
- ...

If required input or tool output is missing, stop and report the issue.

## Workflow

### Step 1: Validate Input

Validate `$required_input`.

### Step 2: Delegate Specialist Work

Invoke the appropriate agent with a narrow prompt.

### Step 3: Apply Reusable Method

Invoke the appropriate skill for templates, checks, or fixed output.

## Failure Conditions

Stop if:
- ...

Continue but mark uncertainty if:
- ...

## Output Summary

Return:
- What was requested
- What was done
- Output artifacts, if any
- Uncertainty or failures
```
