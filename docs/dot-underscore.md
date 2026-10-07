# ._* files

A `._*` file is a hidden file that macOS creates next to a regular file, for example `._report.pdf` next to `report.pdf`. It holds the same Mac-specific metadata as an [.AppleDouble](./apple-double.md) folder, but as a single file for each original file.

It appears whenever a Mac writes to a file system that can't store this metadata itself, most commonly USB sticks and external drives formatted as FAT32 or exFAT, SMB network shares, and ZIP or tar archives created on a Mac.

## Should it be included in the .gitignore?

Yes. `._*` files are generated automatically and useless to anyone else. They double the number of files in a folder, add noise to diffs and pull requests, and cannot be merged sensibly, since they are binary files.

## Snippet

```gitignore
._*
```
