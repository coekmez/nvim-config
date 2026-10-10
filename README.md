# nvim-config

My Neovim config, based on [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim).
Plugins are managed with the built-in `vim.pack`. Colors come from the terminal theme
(`termguicolors` is off).

Requires the latest stable Neovim.

## Install

Back up any existing config first (`~/.config/nvim`, `~/.local/share/nvim`).

### macOS

```sh
brew install neovim git make ripgrep fd tree-sitter-cli unzip
```

### Linux (Ubuntu/Debian)

```sh
sudo add-apt-repository ppa:neovim-ppa/unstable -y
sudo apt update
sudo apt install make gcc ripgrep fd-find tree-sitter-cli unzip git xclip neovim
```

Fedora: `sudo dnf install -y gcc make git ripgrep fd-find tree-sitter-cli unzip neovim`
Arch: `sudo pacman -S --needed gcc make git ripgrep fd tree-sitter-cli unzip neovim`

### WSL

From Windows, install and enter WSL, then follow the Ubuntu steps above:

```sh
wsl --install
wsl
```

### Clone the config

```sh
git clone https://github.com/coekmez/nvim-config.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
nvim
```

Plugins install on first start.

## Notes

- Optional: a [Nerd Font](https://www.nerdfonts.com/) for icons (set `vim.g.have_nerd_font = true` in `init.lua`).
- Update plugins: `:lua vim.pack.update()` (`:write` applies, `:quit` cancels).
- Uninstall: remove `~/.config/nvim` and `~/.local/share/nvim`.
