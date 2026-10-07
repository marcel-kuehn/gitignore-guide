# Git

This page collects files that Git and related tools leave behind in the working tree and that belong in a `.gitignore`.

## Files

- [*.orig files](./orig-files.md)
- [*.rej files](./rej-files.md)
- [Mergetool temp files](./mergetool-temp-files.md)

## Snippet

```gitignore
# Git
*.orig
*.rej
*_BACKUP_[0-9]*
*_BASE_[0-9]*
*_LOCAL_[0-9]*
*_REMOTE_[0-9]*
```
