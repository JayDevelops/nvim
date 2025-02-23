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
- [Common Neovim Commands](#common-neovim-commands)
- [Cloning & Using This Configuration](#cloning--using-this-configuration)

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

## 🔹 Common Neovim Commands

| Command  | Action                            |
| -------- | --------------------------------- |
| `gg`     | Jump to the beginning of the file |
| `G`      | Jump to the end of the file       |
| `H`      | Jump to the top of the screen     |
| `M`      | Jump to the middle of the screen  |
| `L`      | Jump to the bottom of the screen  |
| `Ctrl-d` | Scroll half a page down           |
| `Ctrl-u` | Scroll half a page up             |
| `Ctrl-f` | Scroll a full page down           |
| `Ctrl-b` | Scroll a full page up             |
| `:%y+`   | Copy entire file to clipboard     |
| `ggVG`   | Select all text in the file       |
| `:w`     | Save the file                     |
| `:q`     | Quit Neovim                       |
| `:wq`    | Save and quit                     |
| `:qa`    | Quit all buffers                  |

---

## 🔹 Cloning & Using This Configuration

If you want to use this Neovim configuration, you can clone the repository and remove the `.git` folder to avoid pushing changes to my remote repository.

```sh
# Clone the repository
git clone https://github.com/JayDevelops/nvim.git ~/.config/nvim

# Navigate into the configuration directory
cd ~/.config/nvim

# Remove the .git folder to detach from the remote repository
rm -rf .git
```

This will allow you to use my Neovim setup without affecting my original repository. 🚀

``
