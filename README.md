# Dark 2026 + Dark+ Highlighting

A VS Code user-settings override for a shared Windows and macOS setup.

This repository:

- keeps the built-in `Dark 2026` theme selected;
- restores `Dark+` syntax highlighting, which is also used by `Dark Modern`;
- leaves all workbench colors, including the editor background, to `Dark 2026`;
- requires no extension, VSIX, build step, or extra dependency.

## Installation

Copy the contents of [`settings.json`](settings.json) into your VS Code User `settings.json` on Windows or macOS. Merge it with existing settings instead of replacing unrelated entries.

Replace this repository's previous `editor.tokenColorCustomizations` entry rather than appending its rules. Remove its previous `editor.semanticTokenColorCustomizations` entry and the `[Dark Modern]` block under `workbench.colorCustomizations`, if present. Other syntax-color overrides can affect the result.

The file explicitly sets `workbench.colorTheme` to `Dark 2026`, which must be available in the installed VS Code version. Syntax overrides apply only to this theme. Semantic highlighting remains enabled; `Dark 2026` already inherits the `Dark+` semantic color rules.

## Source and license

`Dark Modern` inherits its syntax colors from `Dark+`. The settings restore the full `Dark+` TextMate rules, including those inherited from `Dark (Visual Studio)`, and override the more specific syntax rules added by `Dark 2026`. Unstyled text keeps the `Dark 2026` editor foreground.

The source is Microsoft Visual Studio Code commit [`e646868227c3e3a9e3f24277c8c7220be42c0be7`](https://github.com/microsoft/vscode/commit/e646868227c3e3a9e3f24277c8c7220be42c0be7), under the [MIT license](https://github.com/microsoft/vscode/blob/e646868227c3e3a9e3f24277c8c7220be42c0be7/LICENSE.txt). Syntax overrides are based on that revision and may need updating if VS Code adds new theme rules; workbench colors follow the installed `Dark 2026` theme.
