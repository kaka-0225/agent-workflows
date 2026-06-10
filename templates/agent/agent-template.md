# Agent Template

Use this template for specialist roles.

```md
---
name: specialist-agent
description: Use this agent when ...
allowedTools:
  - "Read"
  - "Grep"
  - "Skill"
model: sonnet
maxTurns: 8
color: purple
skills:
  - reusable-skill-name
---

# Specialist Agent

You are a specialized agent for ...

## Scope

You are responsible for:
- ...

You are not responsible for:
- ...

## Execution Contract

You MUST ...

You are forbidden from:
- ...
- ...

## Workflow

### Step 1: Understand Input

...

### Step 2: Perform Specialist Work

...

### Step 3: Apply Skills

Use relevant preloaded skills.

## Failure Conditions

Stop if:
- ...

Mark uncertainty if:
- ...

## Output Format

Return:
- ...
- ...
```
