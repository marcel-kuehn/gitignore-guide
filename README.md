# Gitignore Guide

A practical reference for writing `.gitignore` files. This repository combines a wiki explaining what belongs in a `.gitignore` (and why) with a collection of ready-to-use templates, from a universal base template every project should start with to specialized templates for languages, frameworks and project types.

Just as important, it covers what you should **not** put in your `.gitignore`.

## What is a `.gitignore`?

A `.gitignore` file is a plain text file in your repository that tells Git which files and folders it should ignore, meaning Git won't track them, show them as untracked changes or include them in commits. Read more about it in the [official docs](https://git-scm.com/docs/gitignore).

## How to use

1. Copy the [base template](./templates/base.gitignore) into your project as `.gitignore`.
2. Append the templates that match your project type.
3. Check the wiki to understand each entry and adjust it to your project.

## Templates

- [Base](./templates/base.gitignore)

## Wiki

### General

- [.env files](./docs/env.md)
- [macOS](./docs/macos/index.md)
- [Windows](./docs/windows/index.md)
- [Linux](./docs/linux/index.md)
- [Temporary files](./docs/temp-files.md)
- [Git](./docs/git/index.md)
- [Claude Code](./docs/claude/index.md)

## Contributing

Contributions are welcome. Please read the [contributing guide](./CONTRIBUTING.md) before opening an issue or pull request. No AI slop please!

## License

[MIT](./LICENSE).
