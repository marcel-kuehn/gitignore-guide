# Mergetool temp files

When you resolve a conflict with `git mergetool`, Git writes temporary copies of the conflicted file for the merge tool to compare: the common ancestor (`BASE`), your version (`LOCAL`), the incoming version (`REMOTE`) and a backup (`BACKUP`). They sit next to the conflicted file and are named after it, plus the process ID, for example `app_LOCAL_12345.js`.

Git deletes them once the merge tool exits. They stay behind if Git or the merge tool is killed, or if the tool fails and `mergetool.keepTemporaries` is set to `true`.

## Should it be included in the .gitignore?

Yes. These files are leftovers of a merge that is already done and only duplicate versions that are in the history anyway. They have random names and clutter the working tree.

The patterns require a number after the marker, so a regular file like `DATA_LOCAL_cache.json` is not ignored.

## Snippet

```gitignore
*_BACKUP_[0-9]*
*_BASE_[0-9]*
*_LOCAL_[0-9]*
*_REMOTE_[0-9]*
```
