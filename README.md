<div align = "center">

<h1><a href="https://github.com/adityastomar67/nvdots">NVDOTS</a></h1>

<a href="https://github.com/adityastomar67/nvdots/blob/main/LICENSE.md">
<img alt="License" src="https://img.shields.io/github/license/adityastomar67/nvdots?style=flat&color=eee&label="> </a>

<a href="https://github.com/adityastomar67/nvdots/graphs/contributors">
<img alt="People" src="https://img.shields.io/github/contributors/adityastomar67/nvdots?style=flat&color=ffaaf2&label=People"> </a>

<a href="https://github.com/adityastomar67/nvdots/stargazers">
<img alt="Stars" src="https://img.shields.io/github/stars/adityastomar67/nvdots?style=flat&color=98c379&label=Stars"></a>

<a href="https://github.com/adityastomar67/nvdots/network/members">
<img alt="Forks" src="https://img.shields.io/github/forks/adityastomar67/nvdots?style=flat&color=66a8e0&label=Forks"> </a>

<a href="https://github.com/adityastomar67/nvdots/watchers">
<img alt="Watches" src="https://img.shields.io/github/watchers/adityastomar67/nvdots?style=flat&color=f5d08b&label=Watches"> </a>

<a href="https://github.com/adityastomar67/nvdots/pulse">
<img alt="Last Updated" src="https://img.shields.io/github/last-commit/adityastomar67/nvdots?style=flat&color=e06c75&label="> </a>

<!-- <p> -- Github Start Velocity Track
<img src="https://stars.medv.io/adityastomar67/nvdots.svg", title="commits"/>
</p> -->

<h3>Personalized Development Environment ❤️👨‍💻</h3>
  Brief description of how this configuration actually works. Hit the ⭐ button if you found this useful.
</div>

## What is this

Handcrafted `neovim` configs for the ultimate CLI dev experience, completely in `lua`

For a best yet minimal config, go to [minimal.nvim](https://github.com/singhhhx/minimal.nvim/)

## Screenshots
### Dashboard using alpha.nvim
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS01.png"></img>

### Code Conceal
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS02.png"></img>

### When code conceal is off
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS03.png"></img>

### LimeLight for Better focusing
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS04.png"></img>

### File Browsing with nvim-tree and Telescope file_browser extension
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS05.png"></img>

### Git using Lazygit right inside Neovim
<img src="https://github.com/adityastomar67/nvdots/blob/main/bin/img/SS06.png"></img>

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed the latest version of `neovim`
- If having issues, these
[Instructions will help you do that](https://github.com/neovim/neovim/wiki/Installing-Neovim#linux), Checkout complete automated installation script at bottom of the documentation.

#### Before we proceed, File Structure is like

If the reader is well versed or, has a general experience with shell scripting, Lua language or, know what they are doing then they may skip this section. But it advised to take a good understanding of the file structure before making any changes.

```
nvim
├── after
│   ├── indent
│   ├── queries
│   │   ├── cpp
│   │   ├── lua
│   │   └── python
│   └── syntax
├── bin
│   ├── img
│   └── snippets
├── init.lua
├── lua
│   ├── core
│   │   ├── abbreviations.lua
│   │   ├── cmds.lua
│   │   ├── colorscheme.lua
│   │   ├── comment.lua
│   │   ├── consts.lua
│   │   ├── dressing.lua
│   │   ├── files.lua
│   │   ├── keymaps.lua
│   │   ├── options.lua
│   │   ├── plugins.lua
│   │   └── utils.lua
│   └── plugins
│       ├── alpha.lua
│       ├── cmp.lua
│       ├── gitsigns.lua
│       ├── lspInstaller.lua
│       ├── lsp.lua
│       ├── lsp-saga.lua
│       ├── null-ls.lua
│       ├── nvim-tree.lua
│       ├── shared
│       │   └── ascii_art.lua
│       ├── telescope.lua
│       ├── todo.lua
│       ├── toggler.lua
│       ├── toggleterm.lua
│       └── treesitter.lua
└── README.md
```

## Install language servers

Mostly available via npm
```bash
npm install -g typescript typescript-language-server vscode-langservers-extracted vls @tailwindcss/language-server yaml-language-server @prisma/language-server emmet-ls neovim graphql-language-service-cli graphql-language-service-server @astrojs/language-server bash-language-server
```

> TIP: [No sudo on global npm install](https://github.com/sindresorhus/guides/blob/main/npm-global-without-sudo.md)

### Lua, Pyright, Deno, Gopls and rust-analyzer available in Arch/Manjaro repos

Check your package manager for availability if not on an Arch based distro -
_brew, apt_ etc.

```bash
sudo pacman -S lua-language-server pyright deno rust-analyzer gopls shellcheck
```

## Install formatters

[ prettier ](https://prettier.io/) with npm

```bash
npm i -g prettier
```

[ shfmt ](https://github.com/mvdan/sh) is in the AUR

```bash
sudo pacman -S shfmt                        # From the AUR
go install mvdan.cc/sh/v3/cmd/shfmt@latest  # With the help of GO
```

[ stylua ](https://github.com/JohnnyMorganz/StyLua) is in the AUR

```bash
sudo pacman -S stylua
```

Check your package manager for availability if not on an Arch based distro -
_brew, apt_ etc.

[autopep8](https://pypi.org/project/autopep8/) for python is in Manjaro/Arch
repos

```bash
sudo pacman -S autopep8
```

Check your package manager for availability if not on an Arch based distro -
_brew, apt_ etc.

[yamlfmt](https://pypi.org/project/yamlfmt/) for yaml available with pip

```bash
sudo pip install yamlfmt
```

# Installation

```bash
  # move to home dir
  cd ~
  # back up current config
  cp -r ~/.config/nvim ~/.config/nvim.backup
  # clone repository
  git clone https://github.com/adityastomar67/nvdots.git ~/.config
  # Launch nvim for the first time with this command to install plugins
  nvim +PackerInstall
  # exit nvim and Then compile the loader file
  nvim +PackerCompile
```

## Additionals
### Adding custom Snippets

The conifg uses [ luasnip ](https://github.com/saadparwaiz1/cmp_luasnip) paired
with [friendly-snippets](https://github.com/adityastomar67/friendly-snippets), my own fork for VS Code style snippets.
You can add your own snippets to the config [ snippets directory ](./snippets).
You'll also need to edit the [snippets/package.json](./snippets/package.json) to
be able to load your snippets in the correct filetype.
One test snippet is included as an example.

## Plugins

For a list of plugins, see the [plugins file](./lua/core/plugins.lua).

## More Info

Looking for my `zsh` and other `cli` configs? See [Dotfiles](https://github.com/adityastomar67/.dotfiles)

## Resources and inspiration

[Nvim Lua guide](https://github.com/nanotee/nvim-lua-guide)

[Ben Frain has a nice setup](https://gist.github.com/benfrain/97f2b91087121b2d4ba0dcc4202d252f)

[Lunar Vim for inspiration](https://github.com/ChristianChiarulli/LunarVim)

[Ui Customization docs](https://github.com/neovim/nvim-lspconfig/wiki/UI-customization#change-diagnostic-symbols-in-the-sign-column-gutter)

[Lua for Programmers](https://ebens.me/post/lua-for-programmers-part-1/)

[LSP config](https://github.com/neovim/nvim-lspconfig/blob/master/doc/server_configurations.md)

[Awesome list of plugins](https://github.com/rockerBOO/awesome-neovim)

[Plugin Finder](https://neovimcraft.com/)
Noting really, if you have (Neo)vim installed then you can just backup your previous config if any, then just clone this repo and create a symlink of this configuration to your ~/.config/nvim

**SUGGESTION**

* Font: Cascursive - Courtesy of [@sainnhe](https://github.com/sainnhe/icursive-nerd-font) (You can find fonts inside my dotfiles repo)
* [dot_files](https://github.com/adityastomar67/.dotfiles/)
* [Wallpaper](https://github.com/adityastomar67/Wallpapers)

## For Complete Automated install
Run this code snippet in your terminal **(Coming soon...)**
```bash
curl -sL https://bit.ly/Fresh-Install | sh -s -- --vim
```
## TODO
- [ ] Better Documentation
- [x] New Screenshot
- [ ] Get LuaSnip working with dynamic changes enabled
- [ ] Change the keybinding of hopping from "f" to some other key
- [ ] Add hydra plugin
- [x] Changing name to nvdots.
- [ ] Add Mason.nvim
- [ ] Create a version release
- [ ] New Ideas for v2
