---
title: Nerdtree
type: D
tags:
  - Vim
DateStarted: 2023-11-04
DateModified: 2024-04-17
status: 
---

## Install Nerdtree via [Vim-plug](Vim-plug.md)

```lua
-- ~/.config/nvim/init.lua
-- Load Vim-Plug
vim.cmd('source C:/Users/amazi/AppData/Local/nvim/autoload/plug.vim')
-- Load NERDTree
vim.cmd('source C:/Users/amazi/AppData/Local/nvim-data/lazy/nerdtree/lib/nerdtree/nerdtree.vim')
-- Vim-Plug installation: Plugins will be downloaded under the specified directory.
-- vim.cmd [[
--   call plug#begin('C:/Users/amazi/AppData/Local/nvim-data/lazy')
-- ]]
vim.fn['plug#begin']('C:/Users/amazi/AppData/Local/nvim-data/lazy')
-- NERDTree plugin to install
-- vim.cmd [[
--   Plug 'preservim/nerdtree'
-- ]]
vim.fn['plug#']( 'preservim/nerdtree' )
-- Other plugins can be listed here
-- vim.cmd [[
  --   call plug#end()
  -- ]]
vim.fn['plug#end']()
-- NERDTree configuration
-- vim.g['NERDTreeShowHidden'] = 1
```
