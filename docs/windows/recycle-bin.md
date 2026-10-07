# $RECYCLE.BIN/

`$RECYCLE.BIN/` is a hidden system folder that Windows creates at the root of every drive. It holds the files that were deleted on that drive and are waiting in the Recycle Bin.

It only shows up in a repository if the repository sits at the root of a drive, for example on a USB stick or an external disk.

## Should it be included in the .gitignore?

Yes. The folder belongs to the operating system and contains deleted files, not project files. Committing it would add files that were meant to be gone, and could leak their contents.

## Snippet

```gitignore
$RECYCLE.BIN/
```
