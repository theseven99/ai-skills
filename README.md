# AI Skills

A collection of practical, reusable AI agent skills for coding, development workflows, automation, and everyday tasks. Designed to be simple, focused, and easy to install.

This repository contains small, focused skills designed to help AI agents perform specific tasks more effectively. Each skill provides clear instructions and examples that agents can follow in real-world workflows.

The goal is to keep skills **simple, useful, reusable, and easy to install**.

## Available Skills

| Skill | Description |
|---|---|
| [test-in-docker](./skills/test-in-docker/) | Run commands, scripts, and tests inside Docker instead of directly on the host machine. Skip testing when Docker is unavailable. |
| [git-commit-message](./skills/git-commit-message/) | Write an informative Git commit message after completing a task. Never create the commit. |

More skills will be added over time.

## Installation

### Skills CLI (recommended)

Install a specific skill using the [Skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add theseven99/ai-skills --skill test-in-docker
```

```bash
npx skills add theseven99/ai-skills --skill git-commit-message
```

To install all available skills:

```bash
npx skills add theseven99/ai-skills
```

Follow the CLI instructions to select your target agent and installation options.

### Claude Code

Install for the current project:

```bash
mkdir -p .claude/skills
cp -R skills/test-in-docker .claude/skills/test-in-docker
cp -R skills/git-commit-message .claude/skills/git-commit-message
```

Install globally for your user:

```bash
mkdir -p ~/.claude/skills
cp -R skills/test-in-docker ~/.claude/skills/test-in-docker
cp -R skills/git-commit-message ~/.claude/skills/git-commit-message
```

### Codex

Install for the current project:

```bash
mkdir -p .agents/skills
cp -R skills/test-in-docker .agents/skills/test-in-docker
cp -R skills/git-commit-message .agents/skills/git-commit-message
```

Install globally for your user:

```bash
mkdir -p ~/.codex/skills
cp -R skills/test-in-docker ~/.codex/skills/test-in-docker
cp -R skills/git-commit-message ~/.codex/skills/git-commit-message
```

### Other agents

Copy the skill directories into the agent's standard skills directory:

| Agent | Project skills directory | Personal skills directory |
|---|---|---|
| VS Code / GitHub Copilot | `.github/skills/` | `~/.copilot/skills/` |
| Cursor | `.cursor/skills/` | `~/.cursor/skills/` |
| Gemini CLI | `.gemini/skills/` | `~/.gemini/skills/` |

For example, to install `test-in-docker` for VS Code/Copilot in the current project:

```bash
mkdir -p .github/skills
cp -R skills/test-in-docker .github/skills/test-in-docker
```

To install a skill manually, copy or clone this repository, then copy the desired directory, such as `skills/test-in-docker/`, into one of the directories above. Each installed skill directory must contain `SKILL.md` with the skill metadata and instructions.

## Repository Structure

```text
ai-skills/
└── skills/
    ├── test-in-docker/
    │   └── SKILL.md
    ├── git-commit-message/
    │   └── SKILL.md
    └── your-next-skill/
        └── SKILL.md
```

Each skill lives in its own directory and contains a `SKILL.md` file with its instructions, usage guidelines, and examples.

## Adding More Skills

To add a new skill:

1. Create a directory under `skills/`.
2. Add a `SKILL.md` file.
3. Include the skill name, description, instructions, and examples.
4. Keep the skill focused on one clear purpose.

Example:

```text
skills/
└── my-new-skill/
    └── SKILL.md
```

## Design Principles

- **Simple:** Avoid unnecessary complexity and dependencies.
- **Focused:** Each skill should solve a specific problem.
- **Reusable:** Make skills useful across different projects.
- **Practical:** Include clear instructions and real-world examples.
- **Safe:** Respect the user's environment and avoid unnecessary host-side operations.

## Contributing

Suggestions, bug reports, and contributions are welcome.

Feel free to open an issue or submit a pull request to improve an existing skill or contribute a new one.

## License

MIT License. See [LICENSE](./LICENSE) for details.