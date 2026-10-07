# .claude/settings.local.json

`.claude/settings.local.json` holds personal Claude Code settings for one project, such as tool permissions you have approved, environment variables or a different model. It overrides the shared `.claude/settings.json` and your user settings in `~/.claude/settings.json`.

Claude Code creates it when you approve a permission for "this project only", or you create it yourself.

## Should it be included in the .gitignore?

Yes. The file is meant for one developer on one machine, so committing it would force your personal permissions and overrides onto everyone else. It can also contain tokens or local paths set as environment variables.

Claude Code tells git to ignore the file when it creates it, but only on that machine and not if you create the file by hand. An entry in the `.gitignore` covers everyone.

## Snippet

```gitignore
.claude/settings.local.json
```
