---
Title: Vim Basic commands
Type: D
tags:
  - Vim
status: 
DateStarted: 2023-11-06
DateModified: 2023-12-01
mindmap-plugin: basic
---

# Vim Basic commands

## Good

### Buffer (File manipulation)
- Quit
    - `esc` > `:wq`
        - Save and exit
    - `:q`
        - Close the current window
    - `:q!`
        - Quit without saving
- Edit/Open file
    - `:e <path/to/file>`
- Read and merge files
    - `:r [filename]`
        - Insert content of a file specified to the current file below the cursor
    - `:r !ls`
        - Read the output of the ls command and puts it below the cursor
- Save
    - `:w [filename]`
        - Save file to a specified directory
        - Save selected text to a file
    - `:saveas <path/to/file>`
        - Save to the specified path
- Show previous/ next file
    - `:bn`
        - Show next file
    - `:bp`
        - Show previous file

### Insert
- Insert: `i`
- `a`
    - append text after the cursor
- Insert/ Open a new line
    - small `o`
        - Open a line below the cursor
    - big `O`
        - Open a line above the cursor

### Change
- To change until the end of a word (delete and change to insert mode): `ce`
- To change until the end of a sentence: `c$`
- `cw`
    - replace from the cursor to the end of the word
- `c [number] motion`
- To correct mistakes while typing: `backspace`

### Replace
- small `r`
    - Replace the character at the cursor with x(or other character): `rx`
- big `R`
    - To replace more than one character (every typed character deletes an existing  character)

### Delete
- Delete character: `x`
- Delete words: `dw`/ `de`
- To delete 2 words (or a certain number of words): `d2w`
- Delete a whole line and store it in a Vim register: `dd`
- Delete 2 lines: `2dd`
- Delete from cursor to the end of a line: `d$`

### Select
- Press `v` and move cursor
- Select a whole line
    - `V` / `Shift v`

### Indent
- Visual mode: `V >` (Indent) / `V <` (Unindent)

### Move (Basic)
- `e`
    - Move to the next incomplete word
    - go to the end of this WORD.
    - `2w`/ `2e`
        - Move cursor forward 2 words
- `w`
    - Move to the start of next word
    - go to the start of the following WORD
- `0`
    - Move to the start of a line
- `$`
    - go to the end of line
- `j`
    - Move cursor to the end of next line

### Copy
- Select with `v` pressed, and then `y` (yank/ copy) the highlighted text
- `yw`
    - To copy one word
- `yy`
    - To copy the current line

### Put/ Paste
- Put previously deleted line below the cursor: `p`

### Undo
- Undo the last command: `u`
- Undo command on a whole sentence: `U`

### Redo
- `CTRL R`

## Better

### Repeat
- `.` → (dot) will repeat the last command
    - . → Just after the last command will write again the 100 “desu”.
    - `3.` → Will write 3 “desu”
- ⭐`N<command>` → will repeat the command N times.
    - `2dd` → will delete 2 lines
    - `3p` → will paste the text 3 times
    - 100idesu [ESC] → will write desu 100 times

### Move (Go/ Jump)
- `CTRL g`
    - Show the filename and current position/ line number of the file
- `gg` / `G1`
    - Move to the start of the file
- `G`
    - Move to the bottom of the file
- `[line number] G`
    - Go to the line specified
- `CTRL o`
    - Go back to the last position
- `CTRL i`
    - Go forward to the later position
- `fa`
    - go to next occurrence of the letter a on the line
    - `,`
        - will find the next occurence
    - `;`
        - will find the previous occurrence
    - `3fa`
        - find the 3rd occurrence of a on this line
- `t,`
    - go to just before the character `,`
    - `dt"`
        - remove everything until the "
- `F` and `T`
    - like f and t but backward.

### Search
- `/[word]`
    - Move to a word specified/ Search forword
    - To search for the same phrase again
        - `n`
    - To search for the same phrase in the opposite direction
        - N
- ?[word]
    - Search for a phrase in the backward direction
- %
    - Find the matching parenthesis-(, [, or {
- `:s/old/new/gc`
    - To find every occurrence in the whole file with a prompt whether to substitute or not
- Set options
    - `:set ic`
        - Set search result ignore case
    - `/ignore\c`
        - Ignore case for just one search command for the word ignore
    - `:set hls is`
        - Set the `hlsearch`(hightlight search) and `incsearch` options
    - `:set noic`
        - Disable ignoring case
    - `nohlsearch`
        - Disable highlighting matches

### Substitute
- `:s/old/new/g`
    - To replace the word old with new globally
- `:#,#s/old/new/g`
    - To change every occurrence of a character string between two lines where `#,#` are the line numbers of the range of lines

## Stronger

### Move (on current line)
- `^`
    - go to the first non-blank character of the line
- `g_`
    - go to the last non-blank character of line

### Select (Advanced/ Zone selection)
- Suppose the cursor is on the first o of `(map (+) ("foo"))`
    - `vi"` → will select foo.
    - `va"`→ will select "foo".
    - `vi)` → will select "foo"
    - `va)` → will select ("foo").
    - `v2i)` → will select map (+) ("foo")
    - `v2a)` → will select (map (+) ("foo"))
- Select rectangular blocks
    - `CTRL v`
    - `CTRL d`/ use `jjj`
        - move down
    - `I-- [ESC]`
        - write `--` to comment each line
- Select all
    - `ggVG`

### Completion
- CLI completion
    - `CTRL D` + `TAB`
        - Show a list of option and complete
- In insert mode, type the start of the word and press `CTRL n` > `CTRL p`

### Macro
- Create a macro
    - `qa`
        - Record your actions in register `a`
    - q
        - stop recording
- Execute/ play the macro
    - `@a`
        - replay the macro saved in a
    - `@@`
        - a shortcut to replay the last executed macro
- 💡To create lines numbered 1 to 100
    - place cursor on a line containing only the number 1
    - `qa`
        - `yy`
            - copy the line
        - `CTRL a`
            - increment the number
    - `q`
        - stop recording
    - `@a / @@/ 100@@`
        - execute the macro command 100 times

### Splits
- `:split`
- `:vsplit`
    - vertical split the current window

### Help
- `F1`/ `:help`
- `:help [subject]`
    - Find help on any subject
- For more command help
    - `help user-manual`

### Switch window
- `CTRL W`
    - To jump from one window to another

## Execute external command

### `:! [command]`

### `:!ls` (`!dir` on windows)
- To show a list of your directory

### `:!rm [filename]` (`!del [filename]` on windows)
- Remove directory

## 🛠️ Edit *vimrc* file