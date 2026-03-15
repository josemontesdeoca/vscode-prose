# OpenProse for VS Code

Syntax highlighting and snippets for [OpenProse](https://github.com/openprose/prose) `.prose` files.

## Features

- **Syntax highlighting** for all OpenProse constructs — agents, sessions, control flow, pipelines, AI discretion markers, and more
- **Context-aware highlighting** — property names like `model:` and `prompt:` only highlight inside their parent blocks, not in strings or comments
- **Rich string interpolation** — `{variable}` braces and variable names are scoped separately for fine-grained theming
- **Code snippets** for common patterns (type `agent`, `session`, `parallel`, etc. and press Tab)
- **Comment toggling** with `Cmd+/` / `Ctrl+/`
- **Auto-indentation** after block-opening lines
- **Code folding** based on indentation

## Installation

### From VSIX (local install)

1. Download or build the `.vsix` file
2. In VS Code: `Extensions` → `...` menu → `Install from VSIX...`
3. Or from the command line:
   ```bash
   code --install-extension openprose-0.1.0.vsix
   ```

### From Source (for development)

1. Clone this repo
2. Open VS Code and run the `Developer: Install Extension from Location...` command, pointing to the cloned directory
3. Or launch the Extension Development Host:
   ```bash
   code --extensionDevelopmentPath=/path/to/vscode-prose
   ```

## Supported Syntax

| Element | Example |
|---|---|
| Comments | `# this is a comment` |
| Sessions | `session "prompt"` |
| Agents | `agent researcher:` |
| Variables | `let result = session "..."` |
| Parallel | `parallel:` |
| Loops | `for item in items:`, `repeat 3:`, `loop until **done**:` |
| Conditionals | `if **condition**:`, `choice **criteria**:` |
| Error handling | `try:` / `catch:` / `finally:` |
| Pipelines | `items \| map:`, `items \| filter:` |
| Strings | `"hello"`, `"""multi-line"""` |
| Interpolation | `"Hello {name}"` |
| AI discretion | `**evaluated by AI**` |
| Imports | `use "@handle/slug"` |
| IO | `input name: "description"` |

## Editor Compatibility

This extension also works in:
- **Cursor** — works identically (Cursor is a VS Code fork)
- **Any VS Code fork** — same `.vsix` install process

## License

MIT
