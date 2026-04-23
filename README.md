# GitHub Workflows for Zed

A [Zed](https://zed.dev) extension that adds a `GitHub Workflows` language
backed by [tree-sitter-ghactions](https://github.com/rmuir/tree-sitter-ghactions),
a parser for the GitHub Actions expression language (`${{ ... }}`).

## Caveat

`tree-sitter-ghactions` parses GitHub Actions *expressions*, not the
surrounding YAML document. Consequently, highlighting from this extension
applies to the expression language itself — operators, identifiers, context
accessors (`github`, `env`, `secrets`, ...), and builtin functions
(`contains`, `fromJSON`, `hashFiles`, ...). YAML keys and scalars outside
of `${{ ... }}` will not be highlighted by this grammar.

## Installation

Install the extension from Zed's extension registry (`zed: extensions`,
search for "GitHub Workflows"), or install it as a dev extension by cloning
this repo and running `zed: install dev extension`.

## Usage

To associate GitHub Actions workflow files with this language, add the
following to your Zed `settings.json`:

```json
{
  "file_types": {
    "GitHub Workflows": [
      "**/.github/workflows/*.yml",
      "**/.github/workflows/*.yaml",
      "**/.github/actions/**/action.yml",
      "**/.github/actions/**/action.yaml"
    ]
  }
}
```

## License

MIT
