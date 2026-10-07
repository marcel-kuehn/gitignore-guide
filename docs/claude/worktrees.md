# .claude/worktrees/

`.claude/worktrees/` is where Claude Code puts the git worktrees it creates, for example when you start a session with `claude --worktree <name>` or when subagents run in isolation. Each worktree is a full checkout of the repository on its own branch, in a subfolder like `.claude/worktrees/feature-auth/`.

## Should it be included in the .gitignore?

Yes. Without the entry, git in your main checkout lists every worktree as an untracked folder, and a careless `git add .` adds it as an embedded repository. The changes in a worktree are already tracked on its own branch.

## Snippet

```gitignore
.claude/worktrees/
```
