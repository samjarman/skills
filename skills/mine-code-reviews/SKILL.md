---
name: mine-code-reviews
description: Mine the past year of code reviews for improvements to agent guidance and deterministic checks, then open pull requests or merge requests with those improvements.
---

# Mine code reviews

Look back over the past year of code reviews in this repository: every comment, reply, and resulting fix. Read the discussions in context, including how they were resolved. Mine them for recurring lessons that could improve agent guidance such as `AGENTS.md`, or be enforced by deterministic tools such as linting, formatting, and tests. Prefer automated checks where the rule can be reliably enforced; use guidance where judgment is needed. Don't turn one-off preferences or rejected suggestions into general rules. Implement the improvements, run the relevant checks, and open focused pull requests or merge requests using the configured tools and description templates. Link each improvement to the review evidence behind it, and report any gaps in the history you could access.
