
# Robin (Power Automate Desktop) Syntax

Minimal TextMate grammar and language configuration for Power Automate Desktop files (`.robin`, `.pad`).

## Features
- Highlights control keywords (`IF/THEN/END`, `ON ERROR`, etc.)
- Labels (`LABEL foo`)
- PAD action names (e.g. `Display.InputDialog`, `File.ReadTextFromFile.ReadText`)
- Variables, numbers, single/double and triple‑quoted strings (`$'''...'''`)
- Output operator (`=>`) and basic operators
- Single line (`# ...`) and block (`#/ ... #/`) comments
- Region keywords (`**REGION` / `**ENDREGION`) with folding support

## Installation
- From the Marketplace: search for **Robin (Power Automate Desktop) Syntax** (if published).
- Locally: install the built VSIX in VS Code (`Extensions: Install from VSIX...`).

## Development / Testing
1. Open this repository in VS Code.
2. Open a sample `.robin` or `.pad` file (or create one).
3. Run the extension host with the debugger (press `F5`). This opens a new VS Code window using the extension from your workspace.
4. To force grammar changes to take effect in the extension host, use `Developer: Reload Window` in that host window after editing `syntaxes/robin.tmLanguage.json` or `language-configuration.json`.
5. Use `Developer: Inspect Editor Tokens and Scopes` and place the cursor on tokens (quotes, comments, `**REGION`) to confirm the active scopes.

Notes:
- If a file is not using the Robin grammar, click the language mode indicator (bottom-right) and select **Robin** or add a file association in settings.
- Folding markers (regions) must appear as plain lines (not commented) for folding to work.

## Contributing
- Fixes and improvements welcome. Open a PR with focused changes to `syntaxes/` or `language-configuration.json`.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

This is a permissive open-source license that allows you to use, modify, and distribute the software freely, with minimal restrictions.
