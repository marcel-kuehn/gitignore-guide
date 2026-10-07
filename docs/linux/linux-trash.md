# .Trash-* folders

A `.Trash-*` folder is a hidden trash folder that Linux desktops create at the root of a drive, such as a USB stick, an external disk or a second partition. When a file on that drive is moved to the trash, it goes there instead of the trash in the home folder. The suffix is the user ID, so the folder is usually called `.Trash-1000`.

It only shows up in a repository if the repository sits at the root of a drive.

## Should it be included in the .gitignore?

Yes. The folder belongs to the desktop and contains deleted files, not project files. Committing it would add files that were meant to be gone, and could leak their contents.

## Snippet

```gitignore
.Trash-*
```
