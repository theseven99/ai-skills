---
name: git-commit-message
description: After completing a coding task, inspect the changes and provide a concise, informative Git commit message. Never create a commit or run Git commit commands.
---

# Git Commit Message

## Purpose

When a coding task is complete, help the user by writing a commit message that accurately describes the finished changes. Provide the message only; do not make a commit.

## Instructions

1. Review the changes made for the task, including the diff and relevant file names. Do not include unrelated pre-existing changes.
2. Choose a type that best describes the change, such as `feat`, `fix`, `docs`, `refactor`, `test`, `build`, or `chore`.
3. Use a short scope in parentheses when the affected area is clear. Omit the scope when it is not useful.
4. Write a concise summary after the colon, describing the result in imperative, lowercase wording.
5. Add one or more bullet points with useful details when the change involves multiple notable parts. Keep the details specific and avoid repeating the summary.
6. Output only the commit message, with no introduction, explanation, or Markdown code fence.
7. Never create a commit, stage files, or run `git commit`.

## Format

```text
type (scope): summary
- detailed change
- another relevant detail
```

Use the bullets only when they add useful context. For a small change, the summary alone is sufficient.

## Example

```text
feat (web): add account recovery flow
- add a form for requesting a password reset
- show confirmation and validation feedback
```
