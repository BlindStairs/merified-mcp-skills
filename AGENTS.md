# AGENTS.md — merified-mcp-skills

Entry point for anyone working in this repo: humans, and agents of any flavour (Claude, Cursor,
Copilot, Codex…). Start here.

## What this repo is

One publicly installable skill that teaches an agent to consume the Merified MCP well. Nothing
else. See [README.md](README.md) for install and provenance: the authoritative guidance lives
inside the MCP server (`get_merified_guide`), and this repo is a snapshot of it.

## This repository is PUBLIC

Everything committed here is world-readable, permanently. Never add:

- keys, tokens, or any credential
- Supabase project refs
- internal URLs or hostnames
- environment names
- customer, candidate, or employee data
- content copied out of a private repo

Cite private material by path or name only — for example the consumer guide at
`supabase_blindstairs/supabase/functions/mcp-server/MCP_CONSUMER_GUIDE.md` — never paste its
contents. Generic, capability-level guidance is fine; anything that identifies our
infrastructure or our people is not.

## Layout rule

Skills are canonical in `.agents/skills/<name>/`, with per-tool symlinks
(`.claude/skills/<name>`, `.cursor/skills/<name>`) pointing at the canonical directory. Edit the
canonical copy; never replace a symlink with a real directory. Verify with `git ls-files -s` —
the symlinks must be mode `120000`.

## Changes go via PR

Branch, commit, open a pull request; no direct pushes to the default branch. Sign the PR body
with `**Author:** <name>` — the git identity is shared. The skill's guidance is derived content:
a change here that contradicts the in-MCP guide is a bug, not an improvement.

## Cross-repo canon

Company-wide rules are not restated here. They live in `BlindStairs/plane-ops`:

- `../plane-ops/docs/agent-basics.md` — cross-repo agent basics
- `../plane-ops/docs/where-rules-live.md` — which document owns which rule

If that checkout is not beside this one: https://github.com/BlindStairs/plane-ops
