# Aeries SIS Query Support for VS Code

This extension provides syntax highlighting and productivity snippets for the **Aeries SIS Query** language. It is designed to make writing, reading, and debugging school district queries faster and more accurate.

## Features

### 🎨 Syntax Highlighting
* **Commands:** Highlights `LIST`, `TOTAL`, `KEEP`, `SKIP`, `CHANGE`, and more.
* **Table Detection:** Recognizes standard Aeries tables (STU, TCH, SEC, MST, etc.).
* **Aeries Operators:** Distinct colors for the Contains (`:`) and Not Equal (`#`) operators.
* **Description Support:** Highlights the `?` operator used for fetching code descriptions.

### ⚡ Smart Snippets
Type these shortcuts and press `Tab` to instantly generate query structures:
* `stulist` -> `LIST STU NM ID GR IF`
* `keepstu` -> `KEEP STU IF ...`
* `totalgr` -> `TOTAL STU GR BY GR`
* `labels` -> `LABELS STU NM AD CY ST ZP IF ...`

---

## Aeries Query Cheat Sheet

| Operator | Action | Example |
| :--- | :--- | :--- |
| `:` | Contains | `STU.NM : "SMITH"` |
| `;` | Does Not Contain | `STU.NM ; "SMITH"` |
| `#` | Not Equal | `STU.GR # 12` |
| `?` | Description | `STU.ETH?` (Returns "Hispanic" instead of "Y") |
| `\` | Line Break | Used in `LABELS` queries |

---

## Installation

1. Open **VS Code**.
2. Go to the **Extensions** view (`Ctrl+Shift+X`).
3. Click the **...** (More Actions) at the top right.
4. Select **Install from VSIX...**.
5. Select the `aeries-query-syntax-0.0.1.vsix` file.

## Known Issues
* Field highlighting requires the table prefix (e.g., `STU.ID`) for best results.