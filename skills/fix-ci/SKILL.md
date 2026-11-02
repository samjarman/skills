---
name: fix-ci
description: Investigate failing CI logs through MCP, reproduce the failure locally, and fix and push the change when the user asks to fix CI.
---

# Fix CI

CI is failing. Read the failing job's logs through the configured MCP tools and reproduce the failure locally. Fix the cause without weakening the checks, run the relevant checks locally, then commit and push the fix to this branch. Check the new CI run and report the result. If you can't reproduce the failure or verify the result, say what you could and couldn't confirm.
