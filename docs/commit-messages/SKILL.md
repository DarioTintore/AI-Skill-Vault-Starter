---
name: commit-messages
description: Generates clear, structured commit messages following the Conventional Commits convention, starting from the selected diff.
---

# Commit Messages

Generate a commit message following the Conventional Commits convention:

```
<type>(<optional scope>): <short description>

<optional body>
```

Types: feat, fix, docs, refactor, perf, test, build, ci, chore.

Analyze the following diff and propose 2-3 message alternatives, choosing the most suitable one.

```diff
$SELECTION
```
