# Gitignore Guide

[![Checks](https://github.com/marcel-kuehn/gitignore-guide/actions/workflows/checks.yml/badge.svg)](https://github.com/marcel-kuehn/gitignore-guide/actions/workflows/checks.yml)
[![License: MIT](https://img.shields.io/github/license/marcel-kuehn/gitignore-guide)](./LICENSE)

A practical reference for writing `.gitignore` files. This repository combines a wiki explaining what belongs in a `.gitignore` (and why) with a collection of ready-to-use templates, from a universal base template every project should start with to specialized templates for languages, frameworks and project types.

Other template collections give you the patterns. This one also explains every entry, so you know what you're ignoring and can adjust it to your project. Just as important, it covers what you should **not** put in your `.gitignore`.

## What is a `.gitignore`?

A `.gitignore` file is a plain text file in your repository that tells Git which files and folders it should ignore, meaning Git won't track them, show them as untracked changes or include them in commits. Read more about it in the [official docs](https://git-scm.com/docs/gitignore).

## How to use

1. Copy the [base template](./templates/base.gitignore) into your project as `.gitignore`. From the root of your project:

   ```sh
   curl -o .gitignore https://raw.githubusercontent.com/marcel-kuehn/gitignore-guide/main/templates/base.gitignore
   ```

   If you already have a `.gitignore`, append the template instead:

   ```sh
   curl https://raw.githubusercontent.com/marcel-kuehn/gitignore-guide/main/templates/base.gitignore >> .gitignore
   ```

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
