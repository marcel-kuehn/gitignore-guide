# Contributing

Thanks for helping out. This guide explains how entries, wiki pages and templates fit together, so your contribution can be merged without much back and forth.

## Before you start

Small fixes, such as typos or a wrong fact on a wiki page, can go straight into a pull request.

For a new group or a new template, open an issue first. That way we can agree on the scope before you write the pages.

## Adding an entry

Every entry in a template has its own wiki page. When you add one, change all of these:

1. A new wiki page, in the group folder (`docs/<group>/`), or directly in `docs/` if the entry has no group.
2. The group page (`docs/<group>/index.md`): add the page to the file list and the pattern to the snippet.
3. The template, for example `templates/base.gitignore`.
4. The repository's own `.gitignore` if you changed `templates/base.gitignore`. It is a copy of the base template and has to stay identical.
5. `README.md`, but only if you add a new group, template or wiki section.

A new group means a new folder with an `index.md`, a new comment block in the template and a new link in the README.

## Wiki pages

Use the templates as a starting point:

- [Entry page](./docs/_templates/entry-page.md)
- [Group page](./docs/_templates/group-page.md)

Some rules:

- Keep entry pages short. Explain what the entry is and why it belongs in a `.gitignore`, nothing more. [.DS_Store](./docs/macos/ds-store.md) is a good reference for the length.
- Add `## Variations` or `### Exceptions` only when they add something, for example variants of a file name or frameworks that handle a file differently.
- Each page stands on its own: no links to other entry pages and no comparisons with other entries.
- File names are lowercase and hyphenated and describe the entry, for example `ds-store.md` or `linux-trash.md`.

## Templates

- Entries are grouped under a comment heading such as `# macOS`, with a blank line between groups.
- The order inside a group matches the order on the group's wiki page.
- General groups come first, tool-specific groups last.

The base template only contains entries that are safe to ignore in practically every project, regardless of language or tooling: secrets, operating system files, temporary files and leftovers from Git and common tools.

## Writing style

Write the way a colleague would explain it: short sentences, concrete facts, no filler. No AI slop, please. Phrases like "In today's world" or "it's important to note" will be sent back.

## Formatting

Markdown files are formatted with [Prettier](https://prettier.io). Before you open a pull request, run:

```sh
npx prettier@3.9.9 --write "**/*.md"
```

A check on every pull request fails if a file isn't formatted.

## Commits

Commit messages follow [Conventional Commits](https://www.conventionalcommits.org) and fit on one line, for example:

- `docs: add .nfs* files to Linux wiki and base template`
- `docs: fix typo on .DS_Store page`
- `chore: add .gitignore based on base template`
