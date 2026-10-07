# desktop.ini

`desktop.ini` is a hidden system file that Windows Explorer creates when a folder is customized, for example with a custom icon, a different display name or a specific view template. It stores those settings as plain text. Some sync tools, such as Google Drive for desktop, also create it to show their own folder icons.

## Should it be included in the .gitignore?

Yes. `desktop.ini` contains no project information, only local Explorer settings that mean nothing on other machines or operating systems. It is created automatically, often without the user noticing, and only adds noise to commits.

## Snippet

```gitignore
desktop.ini
```
