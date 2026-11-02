---
name: write-skill
description: Draft or refine an agent skill for a repeatable workflow when the user asks to create a SKILL.md or package their working conventions as a skill.
---

# Write a skill

Turn the user's workflow into concise instructions another agent can apply. Preserve their tools, preferences, and intended scope.

## Find the useful context

Use the user's examples and existing project conventions to identify the task, the requests that should trigger it, and the decisions that need guidance. Ask about missing context only when it changes the result. If the workflow is still unclear, draft what is known and make the unresolved choices visible.

## Draft the skill

Create `skills/<name>/SKILL.md` in a skills repository, or use the location the user specifies. Use lowercase letters, digits, and hyphens for the name, matching the directory.

Include YAML frontmatter with `name` and `description`. Describe the capability and when to use it precisely enough to distinguish it from nearby tasks. Put the actual workflow in the Markdown body.

Focus on non-obvious decisions, project context, and constraints. Prefer outcome-based guidance where judgment is useful; specify exact steps where ordering or correctness requires them. Avoid generic advice the agent already knows.

Keep personal conventions easy to find and change. Do not invent tools, policies, approval requirements, or authority to act outside the user's request.

Add references, scripts, or assets only when they serve a concrete need. Link supporting guidance from `SKILL.md` and explain when to read it. Keep private details and credentials out of skills intended for public sharing.

## Check it in practice

Check that the frontmatter is valid and the description identifies realistic trigger requests. In a Vercel skills CLI repository, run `npx skills add . --list` from the root to check discovery when the CLI is available.

Try a representative task within the user's authorized scope. Look for missing context, irrelevant instructions, or overly rigid steps, then revise based on the observed result. Report any checks that could not be completed.
