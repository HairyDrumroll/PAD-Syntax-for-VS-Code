
# Robin (Power Automate Desktop) Syntax

Minimal TextMate grammar and language configuration for Power Automate Desktop files (`.robin`, `.pad`).

This extension provides syntax highlighting and a small language configuration tailored for Power Automate Desktop (PAD) / Robin files. It recognizes and highlights core Robin/PAD constructs such as control keywords (IF/THEN/END, ON ERROR), region markers, labels, PAD action names (for example `Display.InputDialog`, `File.ReadTextFromFile.ReadText`), variables, numbers, and single/double/triple-quoted strings. It also supports comment styles, folding for region markers, and common operators (including the output operator `=>`).

The grammar maps tokens to standard TextMate scopes so themes and other extensions can style PAD files consistently. It's designed to make it easy to paste or author PAD action steps inside VS Code and have them be readable, navigable, and theme-aware.

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

###What is Robin?
[Robin](https://github.com/robin-language/robin) was a Softomotive Robotic Process Automation (RPA) product until it was [purchased by Microsoft in 2020](https://www.microsoft.com/en-us/power-platform/blog/2020/05/19/microsoft-acquires-softomotive-to-expand-low-code-robotic-process-automation-capabilities-in-microsoft-power-automate/), where it has now been merged in to the [Microsoft Power Automate Desktop](https://learn.microsoft.com/en-us/power-automate/desktop-flows/introduction) product.

## Contributing
- Fixes and improvements welcome. Open a PR with focused changes to `syntaxes/` or `language-configuration.json`.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

This is a permissive open-source license that allows you to use, modify, and distribute the software freely, with minimal restrictions.
