# Changelog

Each version of the `merified-mcp` skill, newest first. The fingerprint is the one in the skill's frontmatter.

## 2026-10-31 · fingerprint f6e9029dd5126e0f

- **The skill now activates on its own** when someone asks an agent about Merified (their workday, time off,
  approvals or hiring). It no longer sets `disable-model-invocation`; its description decides when it loads.
- The skill is generated from Merified's knowledge base instead of being written by hand. The frontmatter's `metadata`
  records the generation date and the content fingerprint.
- `SKILL.md` has six sections: when to use it, first calls, scope and selectors, read before you write, writes, and
  safety. Tool names are written `Merified:tool_name`.
- `reference.md` lists every published tool by group with what the person wants to do and how the tool writes. It
  also says what the server does not cover, and gives the app's words in eight languages and the words to avoid.
- Removed:
  - the advice to read a guide tool first (the server no longer has one);
  - the advice to prefer UI links (no tool returns them);
  - the «Last reviewed» date.
