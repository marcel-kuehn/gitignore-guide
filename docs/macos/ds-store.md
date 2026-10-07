# .DS_Store

A `.DS_Store` file (short for "Desktop Services Store") is a hidden file, specific to macOS, that Finder creates in any folder it displays. It stores the view settings of that folder, such as icon positions, window size and position, sort order, the chosen view mode and a custom background. It is created automatically.

## Should it be included in the .gitignore?

Yes. A `.DS_Store` contains no project information, only local Finder state that is meaningless to everyone else. It produces noisy diffs and leads to merge conflicts that cannot be resolved sensibly, since it is a binary file.

It can also leak information, because it keeps a record of file names that were once in the folder, even after those files have been deleted.

## Snippet

```gitignore
.DS_Store
```
