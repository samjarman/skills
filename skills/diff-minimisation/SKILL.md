---
name: diff-minimisation
description: Review the branch diff against the open pull request or merge request's target branch for unnecessary changes when the user asks to minimise the diff.
---

# Diff minimisation

Find the open pull request or merge request for this branch and identify its target branch. Review the diff from their merge base. Is anything unnecessary? Does every change earn its place? Flag changes that could be removed or simplified while preserving the intended behaviour, and explain why. Suggest cuts rather than applying them. If you can't identify the request or target branch, say what's missing rather than guessing.
