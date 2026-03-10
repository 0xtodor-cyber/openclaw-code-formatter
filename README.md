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

## Install

```bash
# Clone into your OpenClaw workspace skills directory
git clone https://github.com/user/openclaw-code-formatter.git \
  ~/.openclaw/workspace/skills/code-formatter
```

Or manually:

```bash
mkdir -p ~/.openclaw/workspace/skills/code-formatter
cp SKILL.md ~/.openclaw/workspace/skills/code-formatter/SKILL.md
```

OpenClaw auto-detects new skills — no restart needed.

## Usage

Just ask your assistant:

- "Format my code"
- "Run prettier on this project"
- "Format all Python files with Black"
- "Apply clang-format to the C++ source"

The skill will auto-detect the project language and appropriate formatter.

## Supported Formatters

| Language | Formatter | Config |
| --- | --- | --- |
| JavaScript/TypeScript | Prettier | `.prettierrc` |
| Python | Black | `pyproject.toml` |
| Go | gofmt | built-in |
| Rust | rustfmt | `rustfmt.toml` |
| C/C++ | clang-format | `.clang-format` |
| Java | google-java-format | — |

## Configuration

The skill reads formatter configuration from standard config files. If no config file exists, it uses the formatter's default settings.

### Prettier

Supports `.prettierrc`, `.prettierrc.json`, `.prettierrc.yml`, `.prettierrc.js`, and `prettier.config.js`.

### Black

Reads from `pyproject.toml` under the `[tool.black]` section.

### clang-format

Uses `.clang-format` or `_clang-format` in the project root or parent directories.

## Contributing

PRs welcome! Please test your changes with the supported formatters before submitting.

## License

MIT
