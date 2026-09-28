# Gitignore Guide

A practical reference for writing `.gitignore` files. This repository combines a wiki explaining what belongs in a `.gitignore` (and why) with a collection of ready-to-use templates, from a universal base template every project should start with to specialized templates for languages, frameworks, and project types.

Just as important, it covers what you should **not** put in your `.gitignore`.

## What is a `.gitignore`?

A `.gitignore` file is a plain text file in your repository that tells Git which files and folders it should ignore, meaning Git won't track them, show them as untracked changes, or include them in commits. Read more about it in the [official docs](https://git-scm.com/docs/gitignore).

## How to use
1. Find a suitable template. If none matches, use the base template.
2. Create a .gitignore file in your project
3. Copy the template into it
4. Read the wiki to understand what you just copied

## Wiki

### General
- [.env files](./docs/env.md)

## Templates
- [Base](./templates/base.gitignore)

## Contributing

Contributions are welcome. Please open an issue or pull request and include a short explanation for any entry you add. Make sure to also extend the wiki.

## License

[MIT](./LICENSE).