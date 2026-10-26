<div align="center">
<p>
    <a>
      <img alt="Linux" src="https://img.shields.io/badge/Linux-%23.svg?style=flat-square&logo=linux&color=FCC624&logoColor=black" />
    </a>
    <a>
      <img alt="macOS" src="https://img.shields.io/badge/macOS-%23.svg?style=flat-square&logo=apple&color=000000&logoColor=white" />
    </a>
    <a>
      <img alt="Windows" src="https://img.shields.io/badge/Windows-%23.svg?style=flat-square&logo=windows&color=0078D6&logoColor=white" />
    </a>
    <a href="https://github.com/neovim/neovim/releases/tag/stable">
      <img src="https://img.shields.io/badge/Neovim-0.12.6-blueviolet.svg?style=flat-square&logo=Neovim&logoColor=green" alt="Neovim minimum version"/>
    </a>
    <a href="https://github.com/karafra/nvim-config/graphs/commit-activity">
      <img src="https://img.shields.io/github/commit-activity/m/karafra/nvim-config?style=flat-square" />
    </a>
    <a href="https://github.com/karafra/nvim-config/graphs/contributors">
      <img src="https://img.shields.io/github/contributors/karafra/nvim-config?style=flat-square" />
    </a>
    <a href="https://github.com/karafra/nvim-config/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/karafra/nvim-config?style=flat-square&logo=GNU&label=License" alt="License"/>
    </a>
    <a href="https://deepwiki.com/karafra/nvim-config">
      <img src="https://deepwiki.com/badge.svg" alt="deepwiki"/>
    </a>
</p>
</div>

# Introduction

This repository hosts a Neovim configuration for Linux, macOS, and Windows.
`init.lua` is the config entry point for terminal Neovim,
and `ginit.vim` is the additional config file for [GUI clients of Neovim](https://github.com/neovim/neovim/wiki/Related-projects#gui).

The configuration is documented to make it easier to understand and adapt.
You can clone the repository and use it, but it is usually better to choose the settings that fit your workflow.

To reduce the possibility of breakage, **this config is only maintained for [the latest Neovim stable release](https://github.com/neovim/neovim/releases/tag/stable).
No effort is spent on maintaining backward compatibility.**

# Install and setup

See [the setup documentation](docs/README.md) for instructions on installing Neovim and its dependencies on Linux, macOS, and Windows.

# Features

+ Plugin management via [Lazy.nvim](https://github.com/folke/lazy.nvim).
+ Code, snippet, and word auto-completion via [nvim-cmp](https://github.com/hrsh7th/nvim-cmp).
+ Language server protocol (LSP) support via [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig).
+ Git integration via [vim-fugitive](https://github.com/tpope/vim-fugitive).
+ Better escaping from insert mode via [better-escape.vim](https://github.com/nvim-zh/better-escape.vim).
+ Ultra-fast project-wide fuzzy searching via [fzf-lua](https://github.com/ibhagwan/fzf-lua).
+ Faster code commenting via [vim-commentary](https://github.com/tpope/vim-commentary).
+ Faster matching pair insertion and jump via [nvim-autopairs](https://github.com/windwp/nvim-autopairs).
+ Smarter matching pair management via [vim-sandwich](https://github.com/machakann/vim-sandwich).
+ Fast buffer jump via [hop.nvim](https://github.com/smoka7/hop.nvim).
+ Powerful snippet insertion via [UltiSnips](https://github.com/SirVer/ultisnips).
+ Beautiful statusline via [lualine.nvim](https://github.com/nvim-lualine/lualine.nvim).
+ File tree explorer via [nvim-tree.lua](https://github.com/nvim-tree/nvim-tree.lua).
+ Better quickfix list with [nvim-bqf](https://github.com/kevinhwang91/nvim-bqf).
+ Search index and count with [nvim-hlslens](https://github.com/kevinhwang91/nvim-hlslens).
+ User-defined mapping hints via [which-key.nvim](https://github.com/folke/which-key.nvim).
+ Asynchronous code execution via [asyncrun.vim](https://github.com/skywind3000/asyncrun.vim).
+ Code highlighting via [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter).
+ Code editing in a browser via [firenvim](https://github.com/glacambre/firenvim).
+ Colorschemes including [gruvbox-material](https://github.com/sainnhe/gruvbox-material).
+ Markdown previewing via [render-markdown.nvim](https://github.com/MeanderingProgrammer/render-markdown.nvim).
+ LaTeX editing and previewing via [vimtex](https://github.com/lervag/vimtex).
+ Notifications via [nvim-notify](https://github.com/rcarriga/nvim-notify).
+ Symbol outline via [aerial.nvim](https://github.com/stevearc/aerial.nvim).
+ Code folding with [nvim-ufo](https://github.com/kevinhwang91/nvim-ufo) and [statuscol.nvim](https://github.com/luukvbaal/statuscol.nvim).

## Nix and Rust

Tree-sitter parsers are installed on demand for Nix (`.nix`) and Rust (`.rs`) files.
If available on `PATH`, the optional `nixd` and `rust-analyzer` language servers are enabled automatically.
Install `nixd` for Nix support and `rust-analyzer` (for example, with `rustup component add rust-analyzer`) for Rust support.

# Shortcuts

Frequently used shortcuts are listed below. `<leader>` represents ASCII character `,`.

| Shortcut          | Mode          | Platform        | Description                                                              |
|-------------------|---------------|-----------------|--------------------------------------------------------------------------|
| `<leader>ff`      | Normal        | Linux/macOS/Win | Fuzzy file searching in a floating window                                |
| `<leader>fh`      | Normal        | Linux/macOS/Win | Fuzzy help file grepping in a floating window                            |
| `<leader>fg`      | Normal        | Linux/macOS/Win | Fuzzy project-wide grepping in a floating window                         |
| `<leader>ft`      | Normal        | Linux/macOS/Win | Fuzzy buffer tag searching in a floating window                          |
| `<leader>fb`      | Normal        | Linux/macOS/Win | Fuzzy buffer switching in a floating window                              |
| `<leader><Space>` | Normal        | Linux/macOS/Win | Remove trailing white spaces                                             |
| `<leader>v`       | Normal        | Linux/macOS/Win | Reselect last pasted text                                                |
| `<leader>ev`      | Normal        | Linux/macOS/Win | Edit Nvim config in a new tabpage                                        |
| `<leader>sv`      | Normal        | Linux/macOS/Win | Reload Nvim config                                                       |
| `<leader>q`       | Normal        | Linux/macOS/Win | Quit current window                                                      |
| `<leader>Q`       | Normal        | Linux/macOS/Win | Quit all windows and close Nvim                                          |
| `<leader>w`       | Normal        | Linux/macOS/Win | Save current buffer content                                              |
| `<leader>y`       | Normal        | Linux/macOS/Win | Copy the entire buffer to the default register                          |
| `<leader>cl`      | Normal        | Linux/macOS/Win | Toggle cursor column                                                     |
| `<leader>cd`      | Normal        | Linux/macOS/Win | Change directory to the current buffer's directory                       |
| `<space>t`        | Normal        | Linux/macOS/Win | Toggle tag window                                                        |
| `<leader>gs`      | Normal        | Linux/macOS/Win | Show Git status                                                          |
| `<leader>gw`      | Normal        | Linux/macOS/Win | Run Git add for current file                                             |
| `<leader>gc`      | Normal        | Linux/macOS/Win | Run git commit                                                           |
| `<leader>gpl`     | Normal        | Linux/macOS/Win | Run git pull                                                             |
| `<leader>gpu`     | Normal        | Linux/macOS/Win | Run git push                                                             |
| `<leader>gbd`     | Normal        | Linux/macOS/Win | Delete a branch                                                          |
| `<leader>gbn`     | Normal        | Linux/macOS/Win | Create a new branch                                                      |
| `<leader>gl`      | Normal/Visual | Linux/macOS/Win | Get permalink for current/visually selected lines                        |
| `<leader>gbr`     | Normal        | macOS           | Browse current Git repo                                                  |
| `<leader>gb`      | Visual        | macOS           | Blame current line                                                       |
| `<F9>`            | Normal        | Linux/macOS/Win | Compile and run current source file                                      |
| `<F11>`           | Normal        | Linux/macOS/Win | Toggle spell checking                                                    |
| `<F12>`           | Normal        | Linux/macOS/Win | Toggle paste mode                                                        |
| `\x`              | Normal        | Linux/macOS/Win | Close location or quickfix window                                        |
| `\d`              | Normal        | Linux/macOS/Win | Close current buffer and go to previous buffer                           |
| `{count}gb`       | Normal        | Linux/macOS/Win | Go to buffer `{count}` or next buffer                                    |
| `{operator}iB`    | Normal        | Linux/macOS/Win | Operate on the whole buffer                                              |
| `Alt-k`           | Normal        | Linux/macOS/Win | Move current line or selected lines up                                   |
| `Alt-j`           | Normal        | Linux/macOS/Win | Move current line or selected lines down                                 |
| `ctrl-u`          | Insert        | Linux/macOS/Win | Turn word under cursor to upper case                                     |
| `ctrl-t`          | Insert        | Linux/macOS/Win | Turn word under cursor to title case                                     |
| `jk`              | Insert        | Linux/macOS/Win | Return to Normal mode                                                    |
| `ZR`              | Normal        | Linux/macOS/Win | Restart Nvim without quitting                                            |

# Custom commands

Additional commands are available alongside those provided by plugins.

| Command      | Description                                                             | Example                        |
|--------------|-------------------------------------------------------------------------|--------------------------------|
| `Redir`      | Capture command output to a tabpage for easier inspection               | `Redir hi`                     |
| `Edit`       | Edit multiple files at the same time, supports globbing                 | `Edit *.vim`                   |
| `Datetime`   | Print current date/time or convert a Unix timestamp                     | `Datetime 12345` or `Datetime` |
| `JSONFormat` | Format a JSON file                                                       | `JSONFormat`                   |
| `CopyPath`   | Copy current file path to clipboard                                     | `CopyPath relative`            |

# Contributing

Contributions and suggestions are welcome.

If you encounter an issue, first try the `:checkhealth` command in Neovim and review the reported messages.
If the problem persists, [open an issue](https://github.com/karafra/nvim-config/issues).

# Further readings

Helpful Neovim resources are documented [here](docs/nvim_resources.md).
