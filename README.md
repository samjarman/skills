# Sam's skills

A growing collection of agent skills, installable with [Vercel's skills CLI](https://github.com/vercel-labs/skills).

## Start here, then make them yours

These skills are a starting point. No good skill can be generic enough to work well for everyone: your projects, tools, standards, and preferences all shape what useful instructions look like.

Yes, install them and try them. Then fork this repo into your own skillset and tweak from there. Keep what helps, change what doesn't fit, and add the context that only you have. The goal is a skillset that reflects how you actually work.

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
npx skills add samjarman/skills --skill write-skill
```

The CLI installs into the current project by default. Add `-g` for a user-wide installation.

## Available skills

| Skill | What it does |
| --- | --- |
| [write-skill](skills/write-skill/SKILL.md) | Turn a repeatable workflow into a focused skill, with useful triggers and room for personal context. |

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
