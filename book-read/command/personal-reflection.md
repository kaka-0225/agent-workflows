---
description: Connect a book idea to personal experience respectfully and without diagnosis.
argument-hint: [book-idea] [user-context]
arguments: book_idea user_context
allowed-tools:
  - Read
  - Agent
  - Skill
model: sonnet
---

# personal-reflection

Guide personal reflection around one book idea and the reader's provided
context.

## Execution Contract

You MUST use `$book_idea` and `$user_context` as the only basis for reflection.

You are forbidden from:

- Diagnosing the user or other people.
- Claiming certainty about motives, trauma, attachment, sexuality, or mental
  health.
- Giving medical, legal, or clinical advice.
- Pressuring the user toward a single conclusion.

## Workflow

1. Validate `$book_idea` and `$user_context`.
2. Invoke `reflection-guide-agent`.
3. Apply `personal-reflection-template`.
4. Apply `evidence-checklist`.

## Failure Conditions

Stop if the book idea or user context is missing.

Mark uncertainty when the reflection depends on missing life context.

## Output Summary

Return:

- Book idea
- User-provided context
- Gentle interpretation
- Reflection questions
- Possible patterns, stated cautiously
- Boundaries and uncertainty
