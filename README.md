# Neovim configuration for C++

## For my FET homies

Konfiguracija napravljena uglavnom iz razloga da ne morate spaliti svoje rožnjače svaki put kada otvorite Amerov docker kontejner ;)

![281107595_547850583540043_6880944970666421911_n](https://user-images.githubusercontent.com/104562710/170366724-51915ac6-a859-4743-acba-a9745b765db7.png)

## Prerequisite dependancies

If you ain't using Arch BTW, then the fuck are you doing here, go to the arch wiki and install it

https://wiki.archlinux.org/title/installation_guide

```
sudo pacman -S nodejs yarn clang python-pip
```
```
pip install pynvim
```

You should also should be using a nerd font in your terminal of choice for the correct drawing of glyphs.

## Install guide

- Open terminal and install the latest neovim version 
sudo pacman -S neovim

- Go to ~/.config and create a dir called nvim

- In the nvim dir create a init.vim file and copy everything from the init.vim file from my repo.

- In the terminal type
```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```
       
- Open the init.vim file with nvim and while in Command mode type :PlugInstall

- Navigate to the directory ~/.local/share/nvim/plugged/coc.nvim and in that directory type
 ```
 yarn install
 ```

- Go back to the directory with the init.vim file, open it with nvim and while in command mode type 
```
CocInstall coc-clangd coc-snippets

```
