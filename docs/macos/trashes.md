# .Trashes folder

A `.Trashes` folder is a hidden folder that macOS creates at the root of external drives, such as USB sticks and external hard drives. When you delete a file on that drive in Finder, it is moved here instead of to the Trash on your main drive. Each user gets a subfolder named after their user ID, for example `.Trashes/501`.

It only shows up in a repository if the repository sits at the root of a drive, or if the contents of a whole drive are copied into one.

## Should it be included in the .gitignore?

Yes. The folder holds files that were deleted on purpose, so they don't belong in the project. It is created automatically and can be large, and committing it could bring back files someone meant to get rid of.

## Snippet

```gitignore
.Trashes
```
