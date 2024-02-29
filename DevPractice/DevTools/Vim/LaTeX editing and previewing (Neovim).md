---
Title: LaTeX editing and previewing (Neovim)
Type: D
tags:
  - Vim
  - LaTeX
DateStarted: 2023-11-07
DateModified: 2023-12-01
status: 
mindmap-plugin: basic
---

# LaTeX editing and previewing (Neovim Vimtex)

## Reference

### https://github.com/lervag/vimtex

### https://www.ejmastnak.com/tutorials/vim-latex/vimtex/

### https://jdhao.github.io/2019/03/26/nvim_latex_write_preview/

### Help
- `:help vimtex-options`
    - used to manually enable, disable, or otherwise configure VimTeX features (e.g. the delimiter toggle list, the compilation method, the PDF reader, etc.)
- `:help g:vimtex_delim_toggle_mod_list`
    - Changing the default delimiter toggle list
- `:help vimtex-syntax`
    - Syntax highlighting
    - `:help vimtex-syntax-packages`
    - `g:vimtex_syntax_packages`
    - `:help vimtex-syntax conceal`
        - replaces various commands, such as math-mode commands for Greek letters, with a shorter Unicode equivalent.
- `:help vimtex-completion`
- `:help vimtex-indent`
- linting and grammar checking
    - `:help vimtex-lint`
    - `:help vimtex-grammar`
- `:help vimtex-navigation`
    - `:help vimtex-toc`
    - `:help vimtex-includeexpr`
        - jump to the TeX source code of packages, style files, and documents included with `\include{}` and `\input{}` using the `gf` shortcut
    - `:help vimtex-latexdoc`
        - access the documentation of LaTeX packages imported with `\usepackage{}` using the `:VimtexDocPackage` command, which is mapped to `K` by default

### ⭐`:help vimtex-default-mappings`
- The command/text object/motion’s `<Plug>` mapping
- The Vim mapping mode (e.g. normal, visual, operator-pending, etc.)
- The action’s default shortcut

### ⭐Insert mode mappings
- 📌`:help vimtex-imaps`
- `\lm`

## Commands

### 📌`:help vimtex-commands`
- cover compilation, PDF reader integration, and system and plugin status

### Info
- `:VimtexInfo`
    - show all relevant info about current LaTeX project
- `\li`
    - info
- `\lI`
    - info full

### Compilation
- `:VimtexCompile`/ `F9`/ `\ll`
    - Compile the current LaTeX source file and opens the viewer after successful compilation
    - `:VimtexStop`
        - Stop compilation for the current project
- vimtex-compile-output
    - `\lo`
- 📌`:help vimtex-compiler`
- ![[z-Assets/Paste image 1699347019386image.png]]
    - https://tex.stackexchange.com/questions/253546/latex-error-file-filename-cls-not-found
- PDF Sync (forward and backward)
    - Jump from .tex source code to PDF viewer
        - `:VimtexView` \ `\lv`
            - Compile and open pdfviewer
    - Backward sync
        - on Sumatra
            - Double click
        - on Zathura
            - Ctrl click
    - Config
        - Ensure your Zathura is SyncTeX-enabled
            - https://www.ejmastnak.com/tutorials/vim-latex/pdf-reader/#ensure-zathura-synctex

### vimtex-doc-package
- `K`

### Cheatsheet
- ![[z-Assets/Paste image 1699585348091image.png]]

## Vimtex (Neovim) Use

### Surrounding environment
- `dse`
    - Delete surrounding environment
- `cse`
    - change surrounding environment
- `tse`
    - Toggle starred environments

### Surrounding commands
- `dsc`
    - delete surrounding commands
- `csc`
    - Change surrounding commands
    - Change boldface text to italic text
        - ![[z-Assets/Paste image 1699325233557image.png]]
- `tsc`
    - Toggle starred commands
    - ![[z-Assets/Paste image 1699325536210image.png]]

### Surrounding delimiters
- `dsd`
    - Delete surrounding delimiters (e.g. (), [], {}, and any of their \left \right, \big \big variants)
- `csd`
    - Change surrounding delimiters
    - ![[z-Assets/Paste image 1699324820294image.png]]
- `tsd`
    - Toggle surrounding delimiters

### Surrounding math
- `ds$`
    - Delete surrounding math
- `cs$`
    - Change surrounding math
    - ![[z-Assets/Paste image 1699324977116image.png]]
- `ts$`
    - Toggle between inline and display math
    - ![[z-Assets/Paste image 1699325587717image.png]]

### Toggle style
- `tsf`
    - Toggle surrounding fractions
- `:VimtexTocToggle`/ `\lT`
    - toggle table of contents window
- `:VimtexTocOpen` \ `lt`
    - show table of contents window

### Motion/ Navigation
- `%`
    - Navigate matching content
- Navigate sections
    - `]]`
        - Jump to the beginning of next section
    - `[[`
        - Jump to the beginning of last section
- Navigate environments
    - `]m`
        - Jump to the next environment `\begin{}` command
    - `[m`
        - Jump to the last environment `\begin{}` command
- Navigate math zones
    - `]n`
        - Jump to next math zone
    - `[n`
        - Jump to last math zone
- Navigate Beamer frames
    - (useful in slide show documents using the beamer document class)
    - `]r`
        - Jump to next frame environment
    - `[r`
        - Jump to last frame environment

### Text Objects (Quick selection)
- `ae`/`ie`
    - Around or Inside LaTeX environments
- `aP`/`iP`
    - Around or Inside sections
- `ad`/ `id`
    - Around or Inside paired delimiters
- `a$`/`i$`
    - Around or Inside inline math
- `ac`/`ic`
    - Around or Inside LaTeX commands

## Supporting Plugins

### Ctags
- jump to the definition of a label with the native Vim shortcut `Ctrl-]`
- to jump back, you can use `Ctrl-T`