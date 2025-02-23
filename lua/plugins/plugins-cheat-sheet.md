# 📌 Neovim Plugin Cheat Sheet

## Table of Contents

- [Mini HiPatterns](#mini-hipatterns)
- [Telescope (Fuzzy Finder)](#telescope-fuzzy-finder)
  - [File & Buffer Navigation](#file--buffer-navigation)
  - [Searching](#searching)
  - [File Browser](#file-browser)
  - [Configuration Highlights](#configuration-highlights)
- [Treesitter](#treesitter)
  - [File Opening & Navigation](#file-opening--navigation)
- [Refactoring](#refactoring)
  - [Incremental Rename](#incremental-rename)
  - [Refactoring Tool](#refactoring-tool)

---

## 🔹 Mini HiPatterns

- **Plugin**: `echasnovski/mini.hipatterns`
- **Event**: `BufReadPre`
- **Functionality**: Enables highlighting of patterns in your code.

---

## 🔹 Telescope (Fuzzy Finder)

- **Plugin**: `telescope.nvim`
- **Priority**: `1000`
- **Dependencies**:
  - `telescope-fzf-native.nvim` (`make` required for build)
  - `telescope-file-browser.nvim`

### 📂 File & Buffer Navigation

| Keybind | Action                                 |
| ------- | -------------------------------------- |
| `;f`    | Find files (respects `.gitignore`)     |
| `\\`    | List open buffers                      |
| `;e`    | Show diagnostics for all buffers       |
| `;s`    | List functions, variables (Treesitter) |

### 🔍 Searching

| Keybind | Action                        |
| ------- | ----------------------------- |
| `;r`    | Live grep (search in project) |
| `;;`    | Resume last Telescope session |

### 📂 File Browser

| Keybind | Action                                          |
| ------- | ----------------------------------------------- |
| `sf`    | Open file browser in current buffer's directory |

### 🛠 Configuration Highlights

- **Default Settings**:
  - `wrap_results = true`
  - `layout_strategy = "horizontal"`
  - `sorting_strategy = "ascending"`
  - `winblend = 0` (no transparency)
- **Pickers**:
  - **Diagnostics**: `theme = "ivy"`, `initial_mode = "normal"`
- **File Browser**:
  - **Overrides `netrw`** (`hijack_netrw = true`)
  - **Normal Mode Shortcuts**:
    - `N` → Create new file
    - `h` → Go to parent directory
    - `<C-u>` → Move selection **up** by 10
    - `<C-d>` → Move selection **down** by 10

---

## 🔹 Treesitter

- **Plugin**: `nvim-treesitter/nvim-treesitter`
- **Version**: `v0.9.1`
- **Ensures Installed**:
  - `javascript`, `typescript`, `css`, `gitignore`, `graphql`, `http`, `json`, `scss`, `sql`, `vim`, `lua`
- **Query Linter**:
  - Enabled ✅
  - Uses virtual text ✅
  - Lints on `BufWrite`, `CursorHold`

### 📂 File Opening & Navigation

| Keybind              | Action                   |
| -------------------- | ------------------------ |
| `:tabnew <filename>` | Open a file in a new tab |
| `gt`                 | Go to the next tab       |
| `gT`                 | Go to the previous tab   |
| `:tabclose`          | Close the current tab    |
| `:tabs`              | List all open tabs       |

---

## 🔹 Refactoring

### ✏️ Incremental Rename

- **Plugin**: `smjonas/inc-rename.nvim`
- **Command**: `:IncRename`
- **Keybinds**:
  | Keybind | Action |
  |---------|--------|
  | `<leader>rn` | Incrementally rename the variable under the cursor |

### 🔄 Refactoring Tool

- **Plugin**: `ThePrimeagen/refactoring.nvim`
- **Functionality**: Enables code refactoring within a visual selection.
- **Keybinds**:
  | Keybind | Action |
  |---------|--------|
  | `<leader>r` | Show refactoring options for the selected code |

---
