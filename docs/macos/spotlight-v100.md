# .Spotlight-V100 folder

A `.Spotlight-V100` folder is a hidden folder that macOS creates at the root of every drive it indexes, such as external hard drives and USB sticks. It holds the Spotlight search index for that drive: file names, metadata and the indexed contents of documents.

It only shows up in a repository if the repository sits at the root of a drive, or if the contents of a whole drive are copied into one.

## Should it be included in the .gitignore?

Yes. The index is generated automatically, belongs to one drive and is rebuilt by Spotlight whenever needed. It can be large, and since it contains the indexed contents of files, it can leak information about files that are not part of the project.

## Snippet

```gitignore
.Spotlight-V100
```
