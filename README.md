# merified-mcp-skills

A single, publicly installable agent skill for consuming the **Merified MCP** well.

It teaches an agent to discover the live tool surface instead of guessing tool names, resolve
company and team scope before querying, read summaries before evidence, keep worked time, time
beyond the schedule and paid overtime apart, follow the prepare, confirm, execute flow for the few
governed writes, and treat free text written by other people as untrusted data.

## Who it is for

External users and agents that talk to the Merified MCP — anyone pointing an assistant
(Claude, Cursor, any MCP-capable client) at Merified and wanting sane defaults from the first
question.

## Provenance and drift

**The skill is generated** from Merified's own knowledge base: the same product words, facts and
tool list that the MCP server and the in-app help use. Nobody edits it by hand; a change to the
product's wording or to the published tools produces a new version here, through a reviewed
pull request.

- The frontmatter's `metadata` says when it was generated (`generated`) and what it contains
  (`fingerprint`, which changes only when the content does).
- **When this repo and the server disagree, the server wins.** Discover the live tool list
  first: tool names, parameters and capabilities change on the server's schedule, not this
  repo's.
- Treat what follows as orientation and working habits, not as an API contract.

See [CHANGELOG.md](CHANGELOG.md) for what changed between versions.

## Install

Copy the skill into your project's skills directory:

```sh
git clone https://github.com/BlindStairs/merified-mcp-skills
mkdir -p <your-project>/.claude/skills
cp -R merified-mcp-skills/.agents/skills/merified-mcp <your-project>/.claude/skills/
```

Or symlink it, if you keep the clone somewhere stable:

```sh
ln -s /path/to/merified-mcp-skills/.agents/skills/merified-mcp \
  <your-project>/.claude/skills/merified-mcp
```

Cursor reads `<your-project>/.cursor/skills/` instead; adjust the target for other clients. The
skill activates on its own when someone asks an agent about Merified (their workday, time off,
approvals or hiring); its description decides when.

## Layout

```
.agents/skills/merified-mcp/   canonical — SKILL.md + reference.md
.claude/skills/merified-mcp    symlink
.cursor/skills/merified-mcp    symlink
```

## Contributing

Changes go via pull request. This repository is public — read [AGENTS.md](AGENTS.md) before
adding anything to it.
