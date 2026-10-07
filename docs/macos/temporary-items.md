# .TemporaryItems folder

A `.TemporaryItems` folder is a hidden folder that macOS creates at the root of external drives and network volumes. Apps use it for temporary files when they work with documents on that drive, for example to write a new version of a file before it replaces the old one. These files are normally deleted right away.

It only shows up in a repository if the repository sits at the root of a drive, or if the contents of a whole drive are copied into one.

## Should it be included in the .gitignore?

Yes. The folder only holds temporary working files that are created automatically and are useless to anyone else. If an app crashes, leftovers can stay behind and end up in a commit by accident.

## Snippet

```gitignore
.TemporaryItems
```
