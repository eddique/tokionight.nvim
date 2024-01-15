# eddique/tokionight.nvim

### Mac Installation

Note - the default terminal on Macbooks only support 16bit colors, in order for colorschemes to display correctly on a Mac, you will need a terminal that supports 24bit color such as iTerm.

1. Remove previous config
```sh
rm -rf ~/.local/share/nvim/lazy

rm -rf ~/.config/nvim
```

2. Clone the repo to your nvim config
```sh
git clone https://github.com/eddique/tokionight.nvim ~/.config/nvim
```

3. Open Neovim
```sh
nvim .
```

Your configuration will begin loading.

### Adding LSPs

Utilize :Mason to install LSP plugins. In nvim:
```sh
:Mason
```

Select the LSP for the language, and hit i to install.

### Config Structure

This may be helpful if you are new to lua and configuring nvim
```sh
.
├── README.md
├── init.lua # configurations imported here for use
└── lua
    └── core
        ├── keymaps.lua # keymaps for motions
        ├── plugin_config # configurations for plugins
        │   ├── init.lua # imports all plugins
        │   ├── lsp.lua # LSP plugin configs
        │   ├── nvim-cmp.lua # nvim-cmp plugin configs
        │   ├── telescope.lua # telescope plugin configs (fuzzy searching)
        │   └── treesitter.lua # treesitter plugin configs
        └── plugins.lua # package manager, plugins installed here
```