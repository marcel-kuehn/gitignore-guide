# .AppleDouble folder

An `.AppleDouble` folder is a hidden directory that stores Mac-specific file metadata on file systems that can't hold that metadata themselves.

It appears inside any directory on a network share or external drive that a Mac has accessed, most commonly on Linux servers and NAS devices (such as Synology or QNAP) that use [Netatalk](https://netatalk.io) to share files over AFP.

For every file in the parent directory, the folder holds a matching file with that file's metadata: resource forks, Finder info (color tags, custom icons, comments), and extended attributes such as the "downloaded from the internet" quarantine flag. macOS reads and writes these files automatically, so you never edit them by hand.

On other file systems, such as external drives formatted as FAT32 or exFAT, macOS stores the same metadata in [._* files](./dot-underscore.md) next to each file instead.

## Should it be included in the .gitignore?

Yes. `.AppleDouble` folders are generated automatically, specific to one machine and file system, and useless to anyone else. Committing them only adds noise to diffs and pull requests, and they can accidentally leak local details such as file origins.

## Snippet

```gitignore
.AppleDouble
```
