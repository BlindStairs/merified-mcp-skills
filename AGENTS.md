# AGENTS.md — merified-mcp-skills

Entry point for anyone working in this repo: humans, and agents of any flavour (Claude, Cursor,
Copilot, Codex…). Start here.

## What this repo is

One publicly installable skill that teaches an agent to consume the Merified MCP well. Nothing
else. See [README.md](README.md) for install and provenance: the skill is generated from
Merified's knowledge base, and the live MCP server stays authoritative.

## This repository is PUBLIC

Everything committed here is world-readable, permanently. Never add:

- keys, tokens, or any credential
- Supabase project refs
- internal URLs or hostnames
- environment names
- customer, candidate, or employee data
- content copied out of a private repo

Never paste the contents of internal material here — and do not name internal repositories,
directory paths, service names or document titles either. A path is itself infrastructure
detail. Generic, capability-level guidance is fine; anything that identifies our systems or our
people is not. When internal guidance is the reason for a change, say so in the pull request,
which is where that context belongs.

## Layout rule

Skills are canonical in `.agents/skills/<name>/`, with per-tool symlinks
(`.claude/skills/<name>`, `.cursor/skills/<name>`) pointing at the canonical directory. Edit the
canonical copy; never replace a symlink with a real directory. Verify with `git ls-files -s` —
the symlinks must be mode `120000`.

## Changes go via PR

Branch, commit, open a pull request; no direct pushes to the default branch. Sign the PR body
with `**Author:** <name>` — the git identity is shared. The skill is generated content: do not
edit `SKILL.md` or `reference.md` by hand. A wrong sentence is fixed where it is generated, and the
next generated version lands here through a pull request reviewed by a person (never
auto-merged). Record each version in [CHANGELOG.md](CHANGELOG.md).

## Cross-repo canon

Blindstairs' company-wide agent rules are not restated here, and they are not public. If you work
at Blindstairs you already know where they live; if you do not, they are not needed to use this
skill.
