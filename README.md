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

**The authoritative, actively maintained guidance lives inside the MCP server itself**: its live
tool list and tool descriptions and, on server versions that offer one, a guide tool. This
repository is a point-in-time snapshot derived from that guidance, first published 2026-06-22.

- **Discover the live tool list first, and read the server's guide tool if it lists one.** They
  describe the server you are actually connected to.
- **When this repo and the server disagree, the server wins.** Tool names, parameters and
  capabilities change on the server's schedule, not this repo's.
- Treat what follows as orientation and working habits, not as an API contract.

Last reviewed: 2026-10-29.

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
skill sets `disable-model-invocation: true`, so it loads when you ask for it rather than firing
on its own.

## Layout

```
.agents/skills/merified-mcp/   canonical — SKILL.md + reference.md
.claude/skills/merified-mcp    symlink
.cursor/skills/merified-mcp    symlink
```

## Contributing

Changes go via pull request. This repository is public — read [AGENTS.md](AGENTS.md) before
adding anything to it.
