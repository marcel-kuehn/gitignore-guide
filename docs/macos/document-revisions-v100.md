# .DocumentRevisions-V100 folder

A `.DocumentRevisions-V100` folder is a hidden folder that macOS creates at the root of a drive. It stores the version history of documents edited in apps that use Auto Save, such as Pages, Numbers, Keynote, TextEdit and Preview. "Browse All Versions" in the File menu reads from it.

It only shows up in a repository if the repository sits at the root of a drive, or if the contents of a whole drive are copied into one.

## Should it be included in the .gitignore?

Yes. The folder is managed by macOS, only works on the Mac that wrote it and can grow large, since it keeps full copies of old document versions. Those old versions can also contain content that was deliberately removed from a document.

## Snippet

```gitignore
.DocumentRevisions-V100
```
