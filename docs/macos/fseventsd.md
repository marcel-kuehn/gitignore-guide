# .fseventsd folder

A `.fseventsd` folder is a hidden folder that macOS creates at the root of every drive it mounts with write access. It holds the FSEvents log, a record of which folders on the drive have changed. Spotlight, Time Machine and other apps use it to find out what changed since they last looked, without scanning the whole drive.

It only shows up in a repository if the repository sits at the root of a drive, or if the contents of a whole drive are copied into one.

## Should it be included in the .gitignore?

Yes. The log is written automatically, changes constantly and only means something to the Mac that wrote it. It consists of binary files, and it records the paths of folders on the drive, including ones outside the project.

## Snippet

```gitignore
.fseventsd
```
