---
title: Debug Neovim can't load Python, even though everything is installed.
Type: D
tags:
  - Vim
status: ✅Done
DateStarted: 2023-11-03
DateModified: 2023-12-01
---

### Debug: Neovim can't load Python, even though everything is installed.

- 🐛Neovim can't load Python, even though everything is installed.

  - 🛠️ Neovim check module issues:
    - In Command Prompt, type: `nvim`
    - Then in Neovim, type: `:checkhealth`
    - Follow the advice to update _pynvim_ module
    - 📌[Neovim on Windows can't find python provider - Stack Overflow](https://stackoverflow.com/questions/65160481/neovim-on-windows-cant-find-python-provider)
  - 🛠️ Add _path-to-python.exe_ to system environment variables
    - Make sure python version is python3.11 (not python3.12)
      - 📌[Python: ModuleNotFoundError: No module named 'imp' · Issue #493 · aws/aws-elastic-beanstalk-cli · GitHub](https://github.com/aws/aws-elastic-beanstalk-cli/issues/493)
  - 🛠️ Neovim config file (Set `g:python3_host_prog`) :
    - Option 1: _init.vim_
      - `let g:python3_host_prog='D:/Users/amazi/AppData/Local/Programs/Python/Python311/python.exe'`
    - Option 2: _init.lua_
      - `vim.g.python3_host_prog ='D:/Users/amazi/AppData/Local/Programs/Python/Python311/python.exe'`
  - 🐛Can't find _pynvim_ module
    - 💡Cause: Python `imp` module missing in python 3.12
      - Install an older version of python: python 3.11
      - `bash` > `sudo apt get python3.11`
  - 🐛Could find `python3` while only `python` command works

    - Create _python.bat_ and _python3.bat_
    - Add
    -

    ```bat
    @echo off
    D:\Users\amazi\AppData\Local\Programs\Python\Python311\python.exe %*
    ```

  - Check the result
    - `python3 --version`
