# Thumbs.db

`Thumbs.db` is a hidden system file that Windows Explorer creates in folders containing images or videos. It caches the thumbnails shown in the thumbnail view, so Explorer doesn't have to generate them again each time the folder is opened.

Since Windows Vista, thumbnails are normally stored in a central cache in the user profile instead. Explorer still creates `Thumbs.db` on network shares and in some other cases, so it keeps turning up in repositories.

## Should it be included in the .gitignore?

Yes. `Thumbs.db` contains no project information, only a local cache that Windows can rebuild at any time. It is a binary file, so changes to it can't be merged and only produce noisy diffs.

It can also leak information, because it may still hold thumbnails of images that have since been deleted from the folder.

## Snippet

```gitignore
Thumbs.db
```
