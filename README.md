# The Robius Book

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

The book source files use [cspell](https://github.com/streetsidesoftware/cspell) for spell checking.
`cspell` can be run through `node` or as a Visual Studio Code [extension](https://github.com/streetsidesoftware/vscode-spell-checker).
Valid words can be added to the `cspell` dictionary by adding the word to the `words` array in the `book\cspell.json` configuration file.
Words to be ignored can be added to the `ignoreWords` array.
Settings that are only applicable to a specific file can be added as inline comments.
