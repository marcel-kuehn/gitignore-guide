# *.rej files

A `*.rej` file holds the parts of a patch that could not be applied. `git apply --reject` and the `patch` command apply what they can and write the failed hunks next to the target file, for example `app.js.rej`, so you can apply them by hand.

## Should it be included in the .gitignore?

Yes. A `*.rej` file is a working file for fixing a failed patch by hand. Once the changes are applied, it is useless, and it should never end up in a commit.

## Snippet

```gitignore
*.rej
```
