<!--
SPDX-FileCopyrightText: 2024 blinry <mail@blinry.org>
SPDX-FileCopyrightText: 2024 zormit <nt4u@kpvn.de>

SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Neovim plugin for 🍃 [Ethersync](https://github.com/ethersync/ethersync)

> [!IMPORTANT]
>
> This plugin requires at least Neovim 0.7.0 (which was released in 2022).

## Installation

### Manual installation

If you're not using a plugin manager, here's a "quick and dirty" way to install the plugin:

```
git clone https://github.com/ethersync/ethersync-nvim $HOME/.local/share/nvim/site/pack/plugins/start/ethersync
```

### Plugin managers

Usually, you will add the string `"ethersync/ethersync-nvim"` to your plugin manager. Here's some example configuration blocks:

#### Lazy

```lua
{
  "ethersync/ethersync-nvim",
  keys = { { "<leader>j", "<cmd>EthersyncJumpToCursor<cr>" } },
  lazy = false,
}
```

#### pckr.nvim

```lua
{
  "ethersync/ethersync-nvim",
  config = function()
    vim.keymap.set('n', '<leader>j', '<cmd>EthersyncJumpToCursor<cr>')
  end
}
```

### Nix

For testing purposes, you can run an Ethersync-enabled Neovim like this:

```bash
nix run github:ethersync/ethersync#neovim
```

## Confirm the installation

To confirm that the plugin is installed, try running the `:EthersyncInfo` command in Neovim. It should show the message "Not connected to Ethersync daemon."

## Tips

We recommend creating a mapping for the `:EthersyncJumpToCursor` command (for example, `<Leader>j`, which jumps to another user's cursor.
