# CLAUDE.local.md

`CLAUDE.local.md` is a Markdown file with personal instructions for Claude Code in one project, for example your sandbox URLs, preferred test data or how you like to work. Claude Code loads it next to the shared `CLAUDE.md` and reads it last, so your own notes come on top of the team's.

It usually sits in the project root, but Claude Code also picks it up in subfolders.

## Should it be included in the .gitignore?

Yes. The file is written by and for one developer, so it has no place in the shared repository. It often contains local URLs, paths or other details about your setup that others don't need to see.

Claude Code doesn't add it to the `.gitignore` for you in most cases, so the entry is easy to forget.

## Snippet

```gitignore
CLAUDE.local.md
```
