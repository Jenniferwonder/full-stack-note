---
title: vim
tags:
  - TechSkills
DateStarted: 2023-02-17
DateModified: 2023-12-01
status:
mindmap-plugin: basic
---

# Vim (Neovim)

## Why Vim/ Nvim

### [Site Unreachable](https://www.youtube.com/watch?v=-cn3MAovsN4)

### [YouTube](https://www.youtube.com/watch?v=D4YTJ2W5q4Y)

### https://jdhao.github.io/2021/12/31/using_nvim_after_three_years/

### Vim features

- - Integrated spell checker
- - ⭐Text autocompletion
- - Tabbed navigation
- - Multiple windows, which divide the editing area horizontally or vertically.
- - Syntax highlighting depending on the programming language or tags used.
- - Undo and redo commands
- - ⭐Understanding of more than 200 different syntaxes
- - Scripting language for programming extensions
- - ⭐Command, word and filename completion
- - Compression and decompression of files, making it possible to edit compressed files
- - ⭐Recognition of file formats and conversion between them.
- - History of executed commands
- - Macro recording and playback
- - Saving of the configuration between sessions
- - Automatic and manual code folding
- - Optional graphical interface

## Nvim Download and Config

### Config Reference:

- [jdhao-Neovim Configuration](https://jdhao.github.io/2018/11/15/neovim_configuration_windows/)
- [docs](https://github.com/jdhao/nvim-config/tree/master/docs)

### Related notes

- [Windows](../Windows/Windows.md)
- [Linux](Linux)
  - Ubuntu
    - 以管理员身份进入系统/ 重置密码
      - https://blog.csdn.net/zhengxiangwen/article/details/50625986
      - `sudo passwd`
      - `su root`
    - Node & NPM
      - https://juejin.cn/s/ubuntu%20install%20lua-language-server
    - Command
      - tldr
        - to get usage of certain command
    - systemd (to enable)
      - https://learn.microsoft.com/en-us/windows/wsl/systemd
      - In order to use Zathura PDF viewer in wsl

### Install dependencies for Nvim

- Python
  - 🐛✅[Debug Neovim can't load Python, even though everything is installed. 1](Debug%20Neovim%20can't%20load%20Python,%20even%20though%20everything%20is%20installed.%201.md)
- Ctags
  - https://askubuntu.com/questions/796408/installing-and-using-universal-ctags-instead-of-exuberant-ctags/836521#836521
- Ripgrep
  - Be able to run `rg`
  - `sudo apt install ripgrep`
  - https://github.com/BurntSushi/ripgrep
  - [Ripgrep](https://github.com/jdhao/nvim-config/tree/master/docs#ripgrep) : a fast grepping tool, used by several searching plugins
- Nerdfont
  - Windows Terminal
    - https://github.com/microsoft/terminal/releases
  - https://medium.com/nerd-for-tech/neovim-but-its-in-windows-f39f181afaf9
  - https://www.nerdfonts.com/font-downloads
- Linter
  - vint: a vim linter
    - 🐛[Vint-Debug](Vint-Debug.md)
  - [GitHub - Vimjas/vint: Fast and Highly Extensible Vim script Language Lint implemented in Python.](https://github.com/Vimjas/vint)
- VCS Tools
  - 🐛`:checkhealth` > No valid vcs tools
    - https://github.com/dirk-thomas/vcstool
- Lua
  - https://neovim.io/doc/user/lua.html
  - Ubuntu 安装 Lua
    - https://blog.csdn.net/DeliaPu/article/details/114271100
  - Lua-language-server
    - https://github.com/LuaLS/lua-language-server/releases/tag/3.7.2
    - https://luals.github.io/#neovim-install
    - https://jdhao.github.io/2021/08/12/nvim_sumneko_lua_conf/
  - LSP support
    - 📌*nvim-lspconfig*

### Download and upgrage Nvim

- ⭐Install Neovim
  - ✅Install the zip package and extract to the expected location
    - https://github.com/neovim/neovim/releases/tag/stable
    - https://github.com/neovim/neovim/wiki/Installing-Neovim
  - ⚡Remember to add neovim/bin to path
    - On ubuntu > _%HOME%/.bash_profile_
      - Add `export PATH="$HOME/nvim-linux64/bin:$PATH"`
- Check Neovim version
  - ![](z-Assets/Paste%20image%201699077593916image.png)
- Update Neovim
  - on windows
    - On windows cmd (admin)
      - `choco upgrade neovim`
      - Chocolatey
        - a package manager for Windows that automates the process of software installation, configuration, and updating on the Windows operating system. Install Neovim with chocolatey
  - on ubuntu
    - Update on ubuntu (not the latest version)
      - [Medium-Update Neovim Guide](https://medium.com/@leonardormlins/easiest-way-to-update-neovim-on-ubuntu-a283c66d5322#:~:text=We%20are%20going%20to%20use%20the%20apt%20package,sudo%20apt-get%20update%20%24%20sudo%20apt-get%20install%20neovim)
      - https://launchpad.net/~neovim-ppa/+archive/ubuntu/stable

## Nvim customization (Config Directory)

### Location

- Check home directory
  - `echo %userprofile%`
- Check config directory and config file
  - In Neovim: `:echo stdpath('config')`
  - Windows
    - _C:\Users\amazi\AppData\Local\nvim_
  - WSL
    - _/home/jenniferwonder/.config/nvim_
    - In windows explorer, type
      - _\\wsl.localhost\Ubuntu-20.04\home\jenniferwonder_

### Plugin management

- ✅Lazy.nvim
  - _plugin_specs.lua_
  - `:pi`
    - to install plugins
  - https://jdhao.github.io/2023/09/02/from_packer_to_lazy_nvim/
- [Vim-plug](Vim-plug.md)
  - Neovim plugin manager

### Structure

- _init.lua_
- _ginit.vim_
- `./lua`
  - `./config`
  - ✅*globals.lua*
    - `>` _utils.vim_
  - ✅*mappings.lua*
    - Set keyboard shortcuts
    - User-defined mapping hint
      - ✅which-key.nvim
  - ✅*colorschemes.lua*
    - Appearance
      - Color scheme
        - sainnhe/gruvbox-material
      - Animated GUI style notification
        - nvim-notify
  - ⭐*plugin_specs.lua*
  - _custom-autocmd.lua_
  - _utils.lua_
- `./plugin`
  - _abbrev.vim_
  - _commands.vim_
  - _log-autocmds.vim_
- `./viml_conf`
  - ✅*options.vim*
    - Set Neovim options, eg. spell checking
    - Spell checking
      - Insert mode, press `CTRL l`
      - https://jdhao.github.io/2019/04/29/nvim_spell_check/
      - https://castel.dev/post/lecture-notes-1/
    - Relative line number
      - `3j` / `3k`
        - To move down or up three lines relatively
  - ✅*autocommands.vim*
    - Set autogroup/ autocmd
    - Require _plugin_specs_
  - ✅*plugins.vim*
    - `let g:...` Plugin setting
- `./autoload`
  - _utils.vim_
  - _buf_utils.vim_
  - _text_obj.vim_
  - _plug.vim_ (Move to Temp, not used)
- `./after/ftplugin`
- `./ftdetect`
  - _pdc.vim_
  - _snippets.vim_
- `./resources`
- `./my_snippets`
  - Auto-completion and Snippets
    - Command line auto-completion
      - 📌wilder.nvim
        - Neovim cmd auto-complete
        - Reference
          - https://github.com/gelguy/wilder.nvim
        - Config
          - 🐛[wilder_python-vim cmd auto-complete](wilder_python-vim%20cmd%20auto-complete.md)
            - `:checkhealth`
        - Use
          - `TAB` to cycle options
    - Code, snippet, word auto-completion
      - 📌nvim-cmp
    - Snippet insertion
      - 📌Ultisnips
  - Smarter and faster matching pair management
    - ✅vim-sandwich
- `./spell`
  - word reference for spell checking

## ⭐[Vim Basic commands](Vim%20Basic%20commands.md)

### Reference

- Vim - Vi Improved - by Steve Oualline
- [Surviving Your First Week | Online Video Tutorial by thoughtbot](https://thoughtbot.com/upcase/videos/onramp-to-vim-surviving-your-first-week)
- http://iccf-holland.org/click5.html
- [Basic commands for using VIM editor like a Pro](https://iq.opengenus.org/basic-commands-for-vim-editor/)
- [简明 Vim 练级攻略 酷 壳 - CoolShell](简明%20Vim%20练级攻略%20%20酷%20壳%20-%20CoolShell)
- [无插件 Vim 编程技巧 酷 壳 - CoolShell](无插件Vim编程技巧%20%20酷%20壳%20-%20CoolShell)
- [YBlog - Learn Vim Progressively](YBlog%20-%20Learn%20Vim%20Progressively)
- [YBlog - Vim as IDE](YBlog%20-%20Vim%20as%20IDE)

## For Navigation

### Searching

- Project-wide fuzzy searching
  - LeaderF
    - https://jdhao.github.io/2020/08/26/leaderf_nvim_settings/
    - https://github.com/Yggdroot/LeaderF
    - If you input string as 'abc;def', then 'abc' will match the file name and 'def' will match the directory name.
- Show search index and count
  - nvim-hlslens
    - Features
      - helps you better glance at matched information, seamlessly jump between matched instances
    - Reference
      - https://github.com/kevinhwang91/nvim-hlslens
    - 🐛Bug
      - Press `n` at the home menu in Nvim
        - ![](z-Assets/Paste%20image%201699255052203image.png)
      - When first activate search
        - ![](z-Assets/Paste%20image%201699259389091image.png)
- Tags navigation
  - vista

### General editing

- Undo management
  - vim-mundo
- Status line
  - lualine.nvim
- Buffer jump
  - hop.nvim
    - https://github.com/phaazon/hop.nvim
- Faster matching pair insertion and jump
  - delimitMate
- Better escaping from insert mode
  - better-escape.vim
- Quick fix
  - nvim-bqf

### File manager

- ✅nvim-tree.lua
- Neotree
- [Nerdtree](Nerdtree.md)

## For [LaTeX](LaTeX)

### ⭐[LaTeX editing and previewing (Neovim)](<LaTeX%20editing%20and%20previewing%20(Neovim).md>)

### LaTeX Config

- Related Files
  - _viml_conf/ plugins.vim_
  - _after/ ftplugin/ tex.lua_
  - _plugin_specs.lua_
- Prerequisite
  - TeXLive
    - Pre-installation
      - https://www.tug.org/texlive/quickinstall.html#running
    - Post-installation
      - ![](z-Assets/Paste%20image%201699709125337image.png)
      - Add to path
        - https://tex.stackexchange.com/questions/456243/what-is-the-easiest-way-to-set-path-of-updatednew-version-texlive-installation
  - Plugin
    - ==VimTex==
- PDF Viewer Setup
  - SumatraPDF
    - 🐛 SumatraPDF viewer doesn't work (can't not be launched automatically after compilation completed)
      - 注意配置文件中 Sumatra 路径设置，及软件名拼写
      - 参考
        - `:help g:vimtex_view_method`
          - find an overview of PDF reader possibilities on Windows
        - `:help vimtex-view-sumatrapdf`
        - `:help vimtex-synctex-inverse-search`
        - `:help vimtex-faq-sumatrapdf-wsl`
        - https://vi.stackexchange.com/questions/38101/vimtex-not-opening-sumatrapdf-automatically
      - In Sumatra
        - `cmd /c start /min "" nvim -headless -c "VimtexInverseSearch %l '&f'"`
  - Zathura
    - Shortcut
      - ![](z-Assets/Paste%20image%201699856166701image.png)
      - Inverse color
        - `CTRL R`
    - Command reference
      - `man zathura`
    - systemd (to enable)
      - https://learn.microsoft.com/en-us/windows/wsl/systemd
      - In order to use Zathura PDF viewer in wsl
    - Install Zathura
      - https://installati.one/install-zathura-ubuntu-20-04/
  - 🐛Bug: `VimtexInverseSearch` is not an internal command (When clicking on pdf, the cursor on the .tex file fail to respond)
    - Vimtex 与 Lazy.nvim 的配置冲突问题
    - 参考
      - https://github.com/lervag/vimtex/issues/2698
      - ✅https://github.com/LunarVim/LunarVim/issues/3723
      - https://www.ejmastnak.com/tutorials/vim-latex/pdf-reader/
- Live-preview
  - https://github.com/xuhdev/vim-latex-live-preview
- Customization
  - Example
    - replace the default mapping, `ds$` with convenient `dsm`
      - In config file, write `nmap dsm <Plug>(vimtex-env-delete-math)`

## For Markdown

### Markdown writing and previewing

- vim-markdown
- markdown-preview.nvim

## For Coding

### Code highlighting

- nvim-treesitter

### Code commenting

- vim-commentary

### Code formatting

- Neoformat

### Async code execution

- asyncrun.vim

### Code editing using true nvim inside browser

- firenvim

## For Git

### vim-fugitive
