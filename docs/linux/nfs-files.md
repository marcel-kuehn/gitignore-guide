# .nfs* files

A `.nfs*` file is a hidden file that the NFS client creates on network shares mounted over NFS. When a file is deleted while a program still has it open, the client renames it to something like `.nfs000000000123abcd00000001` instead of removing it, because the server has no other way to keep it available. It is deleted once the last program closes it.

If the program crashes, the machine loses its connection or the client is shut down too early, the file stays behind.

## Should it be included in the .gitignore?

Yes. A `.nfs*` file is a leftover of a deleted file, not part of the project. It is created automatically, has a random name and keeps the full content of the deleted file, so it can be large.

## Snippet

```gitignore
.nfs*
```
