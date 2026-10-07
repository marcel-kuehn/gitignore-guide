# Temporary files

Files ending in `.tmp` or `.temp` are temporary files. Many programs create them while they work, for example editors while saving, installers, build tools and office applications. They are meant to be deleted when the program is done.

If a program crashes or is closed in the middle of its work, they often stay behind in the folder it was working in.

## Should it be included in the .gitignore?

Yes. Temporary files are created automatically and contain intermediate data that is useless to anyone else. Hardly any project uses these extensions for real files, so ignoring them is safe.

## Snippet

```gitignore
# Temporary Files
*.tmp
*.temp
```
