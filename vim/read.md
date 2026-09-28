# Introduction

The Vim room on TryHackMe introduces the Vim text editor and its basic features. Vim is a powerful command-line text editor commonly used in Linux and Unix-based systems.

In this room, I learned how to open and edit files, navigate through text, insert and delete content, search for specific text, and save or exit files using Vim commands.

The main purpose of this room was to become comfortable with Vim and understand its different modes and commands.

# Commands and Tools

## Tool Used

### Vim

Vim is a command-line text editor used to create and modify files.


# Vim Quick Reference Guide

Vim operates primarily in four modes: **Normal** (navigation and editing), **Insert** (typing text), **Visual** (selecting text), and **Command-line** (saving and exiting). 

When you open Vim, you start in **Normal mode**.

---

## 1. Essential Navigation & Modes

| Command | Action | Example / Usage |
| :--- | :--- | :--- |
| `i` | Enter **Insert mode** before the cursor | Type `i`, then start typing text normally. |
| `Esc` | Return to **Normal mode** | Press `Esc` whenever you want to run commands or navigate. |
| `h` `j` `k` `l` | Move left, down, up, right | Press `j` to move down one line, `l` to move right. |
| `w` | Jump forward to the start of the next word | Press `w` twice to jump forward two words. |
| `b` | Jump backward to the start of a word | Press `b` to move back to the start of the previous word. |
| `0` | Jump to the beginning of the current line | Press `0` to move the cursor to column 1. |
| `$` | Jump to the end of the current line | Press `$` to jump directly to the last character of the line. |

---

## 2. Basic Editing Commands

Apply these editing actions in Normal mode:

* **Delete a single character:** Press `x`
  * *Example:* If cursor is on `a` in `cat`, pressing `x` changes it to `ct`.
* **Delete an entire line:** Press `dd`
  * *Example:* Press `dd` on line 5 to cut/remove line 5 completely.
* **Delete a word:** Press `dw`
  * *Example:* Move cursor to the start of a word and press `dw` to remove that word.
* **Undo an action:** Press `u`
  * *Example:* Press `u` right after deleting a line to restore it.
* **Redo an undone action:** Press `Ctrl + r`
* **Copy (Yank) a line:** Press `yy`
* **Paste copied/deleted text:** Press `p` (pastes *after* cursor)
  * *Example:* Press `dd` to cut a line, move to another line, and press `p` to paste it underneath.

---

## 3. Searching & Replacing

Search for patterns or swap text across your document:

* **Search forward:** Type `/` followed by the search term, then press `Enter`.
  * *Example:* `/error` searches forward for "error". Press `n` for next match, or `N` for previous match.
* **Replace in current line:** Type `:s/old/new/g` and press `Enter`.
  * *Example:* `:s/foo/bar/g` replaces every instance of `foo` with `bar` on the current line.
* **Replace globally across file:** Type `:%s/old/new/g` and press `Enter`.
  * *Example:* `:%s/2025/2026/g` replaces every occurrence of `2025` with `2026` in the entire file.

---

## 4. Saving and Exiting

All save and exit commands start with a colon `:` in Normal mode:

* **Save changes:** Type `:w` and press `Enter`
* **Save and quit:** Type `:wq` (or `ZZ`) and press `Enter`
* **Quit without saving:** Type `:q!` and press `Enter` (forces exit, discarding unsaved changes)

---

## Walkthrough Example: Editing a File

### Step 1: Open or create a file
Open your terminal and run:
```bash
vim example.txt



