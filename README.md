A place to store all my general rules and skills for how agents should build software

## How it works

`global/AGENTS.md` holds the global instructions. `global/CLAUDE.md` imports it with `@AGENTS.md`, and `~/.claude/CLAUDE.md` is a symlink to `global/CLAUDE.md`. `~/.claude/skills` is a symlink to `skills/`, so Claude Code loads every skill in that folder.

To change global instructions, edit `global/AGENTS.md`. To add a skill, create `skills/<name>/SKILL.md`. Both take effect in the next new session. Claude Code writes claude.ai skills into `skills/synced/`, which git ignores.

## Setup on a new machine

Move any existing `~/.claude/CLAUDE.md` and `~/.claude/skills` out of the way first, then run:

```bash
gh repo clone Akashamba/accio ~/accio
ln -s ~/accio/global/CLAUDE.md ~/.claude/CLAUDE.md
ln -s ~/accio/skills ~/.claude/skills
```
