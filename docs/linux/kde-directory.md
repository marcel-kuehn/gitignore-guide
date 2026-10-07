# .directory

A `.directory` file is a hidden file that Dolphin, the file manager of the KDE desktop, creates in a folder when its view settings are changed. It stores things like the view mode, sort order, icon size and a custom folder icon as plain text.

## Should it be included in the .gitignore?

Yes. A `.directory` file contains no project information, only local Dolphin settings that mean nothing to anyone else. It is created automatically, often without the user noticing, and only adds noise to commits.

## Snippet

```gitignore
.directory
```
