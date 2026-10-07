# *.orig files

A `*.orig` file is a backup copy of a file. `git mergetool` creates one for every conflicted file it opens, for example `app.js.orig`, holding the file with the conflict markers as it was before you resolved it. Git keeps it by default, unless `mergetool.keepBackup` is set to `false`.

The `patch` command creates them too, when it applies a change to a file that doesn't match the patch exactly.

## Should it be included in the .gitignore?

Yes. A `*.orig` file is a leftover of a merge or patch that is already done, and only duplicates an old state of a file Git already tracks. Without the entry, it shows up as untracked after every resolved conflict and is easy to commit by accident.

## Snippet

```gitignore
*.orig
```
