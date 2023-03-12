# linux-configs


This repository contains config for my Operating system and contains info about how i customized my terminal.


## Terminal

I am using Oh My Zsh as my terminal shell. I have customized it to look like this:

![Terminal](https://raw.githubusercontent.com/Lakshmanshankar/linux-configs/main/example/zsh.png)

and also added some aliases to make my life easier.

## Powerlevel10k

I am using Powerlevel10k as my terminal theme. I have customized it to look like this:
![Terminal](https://raw.githubusercontent.com/Lakshmanshankar/linux-configs/main/examples/zsh.png)

## Zsh autosuggestions

I am using Zsh autosuggestions as my terminal theme. Auto suggestions are shown in the terminal as you type.And it is based on your command history.
[Installation](https://linuxhint.com/use-zsh-auto-suggestions/)

## Zsh syntax highlighting

I am using Zsh syntax highlighting as my terminal theme. It highlights the commands you type to make it easier to read.
[Installation](https://linuxhint.com/enable-syntax-highlighting-zsh/)


## Vim

I Switched to Astrovim from nvChad. Astrovim is a minimalistic vim config. I have customized it to look like this:

![Vim](https://raw.githubusercontent.com/Lakshmanshankar/linux-configs/main/examples/nvim.png)


## Tweaks
I have added some tweaks to make my life easier.

![Vim](https://raw.githubusercontent.com/Lakshmanshankar/linux-configs/main/examples/lakshmanvim.png)


## Features

1. NeoTree -> File explorer
2. Telescope -> Fuzzy finder, ripgrep, live grep // for searching files and code in the entire codebase
3. LSP -> Language server protocol
4. Git -> Git integration
5. Nerd Fonts -> Icons
6. Github Copilot -> AI assisted coding
7. Themes -> Catppuccin, One dark, vscode

Astro includes 50 plugins and 100+ keybindings. It is a minimalistic vim config

## Details

By default Astrovim uses [Nerd Fonts](https://www.nerdfonts.com/).

On top of that I have added the following plugins:
1. I am using Github Copilot for AI assisted coding.
2. By default the dot env and other non programming files are not highlighted. for that You gave to do the following 
in lua/user/init.lua

```lua
    ["neo-tree"] = {
      filesystem = {
        filtered_items = {
          visible = true, 
          hide_dotfiles = false,
          hide_gitignored = true,
        },
      }
    },
```

NeoTree is a file explorer for vim. But some of the files are ignored by default like .env files. So I have added the above code to show all the files.


3. Themes

Astrovim comes with a few themes. I have added the following themes:

The default theme is something simialr to onedark. So Installed the one dark them and  catppuccin theme

To add themes /lua/user/init.lua (it is for own configs this will overwrite the default lua confs)

```lua
plugins = {
    init = {
       "joshdick/onedark.vim",
        "catppuccin/nvim",
        "Mofiqul/vscode.nvim"
    },
    {
      "catppuccin/nvim",
      as = "catppuccin",
      config = function()
        require("catppuccin").setup {}
      end,
    },
```


Once You added the above code to the init.lua file. You have to install the themes using the following command:

```bash 

:PackerInstall

```

To change the theme you have to add the following code to the init.lua file:

```lua
:colorscheme catppuccin #likewise you can change the theme
```
