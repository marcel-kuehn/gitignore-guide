# .claude/agent-memory-local/

`.claude/agent-memory-local/` holds notes that Claude Code subagents write for themselves while they work, such as patterns they found in the codebase or mistakes to avoid next time. Each subagent gets its own folder with a `MEMORY.md`.

Claude Code only creates it for subagents that set `memory: local` in their frontmatter. Subagents with `memory: project` write to `.claude/agent-memory/` instead, which is meant to be committed.

## Should it be included in the .gitignore?

Yes. `memory: local` exists precisely to keep a subagent's memory on your machine. The notes are written automatically and change after every run, so committing them would mean constant noisy diffs.

## Snippet

```gitignore
.claude/agent-memory-local/
```
