# Sam's skills

Short prompts I've developed through work, shared to give you ideas for your own skills.

## More inspiration than installation

These skills are a starting point. They're deliberately brief: enough to get the idea across so you can adapt it to how you work.

No good skill can be generic enough for everyone. Your projects, tools, standards, and preferences shape what useful instructions look like. Read these, borrow the ideas, and write your own versions. You don't need to install anything to get value from them.

You can also install them with [Vercel's skills CLI](https://github.com/vercel-labs/skills). If one is useful, fork it into your own skillset and tweak it from there. Keep what helps and add the context that only you have.

## Available skills

Examples use `/skill-name` shorthand; use your agent's supported invocation syntax.

| Skill | What it does | Invoke like… |
| --- | --- | --- |
| [afk](skills/afk/SKILL.md) | Keep working toward the stated goal while you are away, making assumptions until done or blocked by guardrails. | `/afk` after agreeing on the goal |
| [diff-minimisation](skills/diff-minimisation/SKILL.md) | Review the pull request or merge request diff and ask whether every change earns its place. | `/diff-minimisation` on a branch with an open PR or MR |
| [feedback](skills/feedback/SKILL.md) | Turn a specific correction into an update to agent instructions so the lesson carries forward. | `/feedback You just checked Jira when we use GitLab issues instead.` |
| [fix-ci](skills/fix-ci/SKILL.md) | Read CI logs through MCP, reproduce the failure locally, then fix, verify, and push. | `/fix-ci` on the branch with failing CI |
| [go-harder](skills/go-harder/SKILL.md) | Investigate unverified claims and return with a researched, grounded opinion. | `/go-harder` after an answer with unverified claims |
| [golden-loop](skills/golden-loop/SKILL.md) | Supply a goal and a deterministic check, then let the agent keep working until the check succeeds. | `/golden-loop Goal: fix the login bug. Check: npm run test:login passes.` |
| [meet-brief](skills/meet-brief/SKILL.md) | Compare the branch diff with the ticket and explain whether the work meets the brief. | `/meet-brief Check this branch against issue #123.` |
| [mine-code-reviews](skills/mine-code-reviews/SKILL.md) | Turn lessons from a year of code reviews into agent guidance and automated checks, with PRs or MRs for the improvements. | `/mine-code-reviews` in the repository to review |
| [open-code-review](skills/open-code-review/SKILL.md) | Run checks, fix failures, open a pull request or merge request, and suggest reviewers without assigning them. | `/open-code-review` when your branch is ready for review |
| [pro-con](skills/pro-con/SKILL.md) | Simplify a suggestion and weigh its pros and cons. Good for vibe coders with decision fatigue. | `/pro-con` after a suggestion you want explained |
| [reflect](skills/reflect/SKILL.md) | Review the conversation and update AI guidance with lessons from corrections, friction, and tool failures. | `/reflect` after a session with corrections or friction |

## Install

With Node.js and npm available, list the skills first:

```sh
npx skills add samjarman/skills --list
```

Choose skills and agents interactively:

```sh
npx skills add samjarman/skills
```

Or install one skill:

```sh
npx skills add samjarman/skills --skill reflect
```

The CLI installs into the current project by default. Add `-g` for a user-wide installation.

## Write your own

Each skill lives in its own directory:

```text
skills/
└── your-skill/
    ├── SKILL.md
    ├── references/   # Optional supporting guidance
    ├── scripts/      # Optional executable helpers
    └── assets/       # Optional files used in output
```

Only `SKILL.md` is required. Start a new one with the CLI:

```sh
cd skills
npx skills init your-skill
```

Edit the generated file. Its YAML frontmatter needs a `name` and `description`; the body contains instructions for the agent. Use a lowercase, hyphenated name matching the folder. Describe what the skill does and when to use it.

Keep instructions focused on decisions the agent would otherwise get wrong. Add supporting files only when the workflow needs them, and link to them from `SKILL.md`.

Preview local discovery from the repository root before publishing:

```sh
npx skills add . --list
```

Try the skill on a real task, revise it based on what happens, and add it to the table above. See the [authoring documentation](https://github.com/vercel-labs/skills/blob/main/docs/creating-skills.md) for the format and discovery rules. No npm package or build step is needed.

## Make a personal fork

1. Fork this repository on GitHub and clone your fork.
2. Edit the skills to match your tools, conventions, and preferences.
3. Commit your changes, then install from your own repository:

   ```sh
   npx skills add YOUR-USERNAME/skills
   ```

Point future installs at your fork so your customizations stay with you.

## License

[MIT](LICENSE). Fork, adapt, and share.
