# GitHub Workflows for Zed

A [Zed](https://zed.dev) extension that adds a `GitHub Workflows` language
for GitHub Actions workflow files.

## What it provides

- A language named **GitHub Workflows** backed by the YAML tree-sitter grammar
- Syntax highlighting, bracket matching, outline, and text objects
- Prettier formatting using the `yaml` parser

## Installation

Install the extension from Zed's extension registry (`zed: extensions`, search
for "GitHub Workflows"), or install it as a dev extension by cloning this
repo and running `zed: install dev extension`.

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
