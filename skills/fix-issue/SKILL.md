---
name: fix-issue
description: Use when given a GitHub issue number or URL to analyze, implement, and submit a fix via PR
---

# Fix GitHub Issue

## Overview
Systematic workflow for fixing GitHub issues: understand → plan → implement → verify → submit PR.

## When to Use
- User provides a GitHub issue number or URL
- User says "fix issue #123" or "address this issue"

## When NOT to Use
- Issue requires clarification from the reporter (comment first, don't start implementation)
- Issue is a feature request requiring design decisions (use brainstorming skill first)

## Workflow

### 1. Understand the Issue
```bash
gh issue view $ISSUE_NUMBER
```
- Read the full description and comments
- If unclear, ask user before proceeding or comment on the issue

### 2. Create Branch
Follow git branching rules from CLAUDE.md:
```bash
git checkout -b fix/ISSUE-123-brief-description
```

### 3. Plan the Fix
- Search codebase for relevant files
- **If non-trivial:** Use brainstorming skill to explore approaches
- Create tasks with TaskCreate for tracking

### 4. Implement (TDD)
- **REQUIRED:** Use superpowers:test-driven-development
- Write failing test first
- Implement minimal fix
- Verify test passes

### 5. Verify Before Claiming Done
- **REQUIRED:** Use superpowers:verification-before-completion
- Run full test suite: `npm test`
- Run linting: `npm run lint`
- Run type checking: `npm run typecheck`

**If any verification fails:** Fix issues before proceeding. Do NOT skip to PR.

### 6. Commit and PR
```bash
git add <specific-files>
git commit -m "fix: description of fix

Fixes #123"
git push -u origin HEAD
gh pr create --title "Fix: brief description" --body "Fixes #123

## Summary
- What was wrong
- How it was fixed

## Test Plan
- How to verify the fix"
```

### 7. Cleanup
```bash
git checkout main
```

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Starting implementation on unclear issue | Ask for clarification first |
| Skipping tests | Always use TDD skill |
| Claiming "fixed" before verification | Run all checks, confirm output |
| Committing unrelated files | Use specific file names in git add |
