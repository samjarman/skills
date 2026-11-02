---
name: open-code-review
description: Run the project's deterministic checks, fix failures while preserving the intent of the change, and open a pull request or merge request when the user asks to prepare a change for review.
---

# Open code review

Explore the codebase for deterministic checks, such as linting, formatting, and tests. Run the relevant checks and modify the code until they pass, preserving the intent of the change. If a check cannot be completed, report what blocked it.

Open a merge request or pull request using the configured tools, following any description templates. Include the checks run and their results.

Use `git blame` on the touched files to suggest reviewers to the user, explaining their connection to the changed code. Do not assign reviewers or request their reviews yet.
