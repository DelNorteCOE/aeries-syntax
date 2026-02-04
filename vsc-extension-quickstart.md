# Welcome to your Aeries SIS Query Extension

## What's in the box
* **Syntax Highlighting**: Custom rules for Aeries-specific commands (`LIST`, `KEEP`), operators (`:`, `#`, `?`), and table codes (`STU`, `SEC`).
* **Snippets**: Productivity shortcuts for common queries like `stulist` and `totalgr`.
* **Language Support**: Automatic recognition for `.aeries` and `.aqy` files.

## Running the Extension for Testing
1.  Open this folder in VS Code.
2.  Press `F5`. This opens a new **Extension Development Host** window.
3.  In the new window, create a new file and save it as `test.aeries`.
4.  Type `LIST STU NM` and verify that the colors appear correctly.
5.  Type `stulist` and press `Tab` to test the snippets.

## Making Changes
* **Adding Tables**: To add more Aeries tables (like `ENR` or `PGM`), open `syntaxes/aeries.tmLanguage.json` and add them to the `entity.name.tag.table.aeries` match list.
* **Adding Snippets**: To add new query shortcuts, update `snippets.json`.
* **Applying Changes**: After saving changes to your JSON files, go back to the **Extension Development Host** and press `Ctrl+R` (or `Cmd+R` on Mac) to reload and see the updates immediately.

## Packaging for Others
When you are ready to share the installer:
1.  Ensure `vsce` is installed: `npm install -g @vscode/vsce`
2.  Run `vsce package` in the terminal.
3.  Share the resulting `.vsix` file with your colleagues.

## Useful Aeries Logic Reminders
* `:` = Contains (SQL LIKE)
* `;` = Does not contain
* `?` = Description operator
* `\` = Line break for labels