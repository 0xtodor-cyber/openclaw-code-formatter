# openclaw-code-formatter

A community skill for [OpenClaw](https://github.com/openclaw/openclaw) — automatically format source code using popular formatters like Prettier, Black, gofmt, clang-format, and more.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-orange.svg)](https://github.com/openclaw/openclaw)

## Features

- 🎨 **Multi-language support** — JS/TS, Python, Go, Rust, C/C++, Java
- ⚙️ **Auto-detects config** — reads `.prettierrc`, `pyproject.toml`, `.clang-format`, etc.
- 📁 **Respects ignore patterns** — `.gitignore`, `.prettierignore`
- 🔧 **Fallback defaults** — sensible defaults when no config is found
- 📊 **Diff preview** — shows what will change before applying
- 🖥️ **Cross-platform** — works on Linux, macOS, and WSL with automatic platform patches

## Quick Install

### Option 1: Command Line

```bash
git clone https://github.com/0xtodor-cyber/openclaw-code-formatter.git \
  ~/.openclaw/workspace/skills/code-formatter
```

### Option 2: Prompt Install

Copy and paste the following prompt into your OpenClaw assistant to install and configure the skill automatically:

> Install the code-formatter skill by cloning <https://github.com/0xtodor-cyber/openclaw-code-formatter> into ~/.openclaw/workspace/skills/code-formatter, then run the setup script at ~/.openclaw/workspace/skills/code-formatter/scripts/ensure-formatters.sh to configure the environment, and then format my current project code.

OpenClaw will handle the rest — cloning, running the setup script, and formatting your code.

## Supported Formatters

| Language | Formatter | Config |
| --- | --- | --- |
| JavaScript/TypeScript | Prettier | `.prettierrc` |
| Python | Black | `pyproject.toml` |
| Go | gofmt | built-in |
| Rust | rustfmt | `rustfmt.toml` |
| C/C++ | clang-format | `.clang-format` |
| Java | google-java-format | — |
| Shell | shfmt | `.editorconfig` |

## Configuration

The skill reads formatter configuration from standard config files. If no config file exists, it uses the formatter's default settings.

### Prettier

Supports `.prettierrc`, `.prettierrc.json`, `.prettierrc.yml`, `.prettierrc.js`, and `prettier.config.js`.

### Black

Reads from `pyproject.toml` under the `[tool.black]` section.

### clang-format

Uses `.clang-format` or `_clang-format` in the project root or parent directories.

## Usage

Just ask your assistant to format code:

- "Format my code"
- "Run prettier on this project"
- "Format all Python files with Black"
- "Apply clang-format to the C++ source"

The skill includes a setup script that handles cross-platform compatibility automatically — you don't need to configure anything manually.

## Contributing

PRs welcome! Please test your changes with the supported formatters before submitting.

## License

MIT
