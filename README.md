# Verse Grammar

TextMate grammar for the Verse programming language developed by Epic Games.

## What it is

A TextMate grammar (scope `source.verse`) for `.verse` files. Verse is a programming language designed for metaverse experiences, primarily used in Unreal Engine and Fortnite Creative (UEFN).

This grammar is designed to be used with GitHub Linguist for syntax highlighting on GitHub: Verse support was added to Linguist in [github-linguist/linguist#7440](https://github.com/github-linguist/linguist/pull/7440), with this repository as the grammar source for `source.verse`.

## Features

- Syntax highlighting for `.verse` files (`grammars/verse.tmLanguage.json`, scope `source.verse`)
- Comment support: line `#` and nested block `<# #>` comments, plus indented comment blocks
- Basic language constructs recognition: keywords, specifiers, definitions, function calls, numbers (including hexadecimal and units), characters, strings with escapes and `{}` interpolation, module paths such as `/Verse.org/Simulation`, and Verse markup
- Bracket matching, auto-closing and surrounding pairs, and comment toggling (`language-configuration.json`)
- A sample file covering common constructs (`samples/sample.verse`)

## Getting started

### Usage

- **On GitHub:** nothing to install. GitHub Linguist uses this grammar to highlight `.verse` files.
- **In a TextMate-compatible editor or highlighter:** load `grammars/verse.tmLanguage.json` and register it for the `.verse` extension with scope name `source.verse`.
- **As a VS Code language contribution:** `package.json` is a VS Code extension manifest that contributes the `verse` language (aliases `Verse`, `verse`, extension `.verse`) with `language-configuration.json` and the grammar above.

## Project structure

| Path | Purpose |
| :--- | :--- |
| `grammars/verse.tmLanguage.json` | The TextMate grammar |
| `language-configuration.json` | Comments, brackets, auto-closing pairs and indentation rules |
| `package.json` | VS Code extension manifest contributing the language and grammar |
| `samples/sample.verse` | Sample Verse source used to check highlighting |

## Credits

This grammar is based on Epic Games' Verse TextMate grammar, also published under CC0 in [verselang/book](https://github.com/verselang/book).

## Tech stack

- TextMate grammar (JSON, Oniguruma regular expressions)
- VS Code language configuration

## License

MIT, see [LICENSE](LICENSE).
