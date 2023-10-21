# The Robius Book

[![Book Action](https://img.shields.io/github/actions/workflow/status/project-robius/book/book.yaml?label=book%20build)](https://github.com/project-robius/book/actions/workflows/book.yaml)
[![Book](https://img.shields.io/badge/view-Robius_Book-blueviolet)](https://project-robius.github.io/book/)
[![Matrix Chat](https://img.shields.io/matrix/robius-general%3Amatrix.org?server_fqdn=matrix.org&style=flat&logo=matrix&label=Matrix%20Chat&color=B7410E)](https://matrix.to/#/#robius:matrix.org)

This directory contains the Robius book, which provides a detailed overview of our vision for multi-platform app dev in Rust.

The book is also where you can find documentation, tutorials, and examples on how to design, build, publish and run applications using the Robius community of projects.

You can browse the book directly starting at [SUMMARY.md](src/SUMMARY.md), the table of contents and first chapter.

The book is written in Markdown and uses [mdBook](https://rust-lang-nursery.github.io/mdBook/) to build a nicely-formatted HTML version of the book.

## Building the book

First, install `mdbook`, version `0.4.13` or higher:
```sh
cargo +stable install mdbook
```

You can optionally install a plugin that checks links when building the book:
```sh
cargo +stable install mdbook-linkcheck
```

From this directory, you can build (and optionally open) the book by running:
```sh
mdbook build --open   # `--open`` will open the book in your browser
```


## Spellcheck

The book source files use [cspell](https://github.com/streetsidesoftware/cspell) for spell checking, which occurs automatically as a GitHub Actions CI pass.

` cspell` can be run locally through `node` or as a Visual Studio Code [extension](https://github.com/streetsidesoftware/vscode-spell-checker).

Valid words that are globally relevant (to multiple files) can be added to the `cspell` dictionary by adding the word to the `words` or array in the [`cspell.json`](cspell.json) configuration file.
Words to be ignored can be added to the `ignoreWords` array.

Exceptions that are only applicable to a specific file can be added as inline comments, either by
* Ignoring entire regions of code:
  ```md
  <!-- cspell:disable -->
  Content that you do not want to spell check.
  <!-- cspell:enable -->
  ```
* Adding this anywhere in the file
  ```md
  <!-- cspell:ignore Mobius, Möbius, ˈɹoʊˈbiəs -->
  ```

