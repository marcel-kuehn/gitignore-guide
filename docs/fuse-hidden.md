# .fuse_hidden* files

A `.fuse_hidden*` file is a hidden file that FUSE file systems create, such as NTFS drives mounted with ntfs-3g or remote folders mounted with sshfs. When a file is deleted while a program still has it open, FUSE renames it to something like `.fuse_hidden0000a1b200000003` instead of removing it right away. It is deleted once the last program closes it.

If the program crashes or the drive is unmounted too early, the file stays behind.

## Should it be included in the .gitignore?

Yes. A `.fuse_hidden*` file is a leftover of a deleted file, not part of the project. It is created automatically, has a random name and can be large, since it keeps the full content of the deleted file.

## Snippet

```gitignore
.fuse_hidden*
```
