# Neovim configuration for C++

Konfiguracija napravljena uglavnom iz razloga da ne morate spaliti svoje rožnjače svaki put kada otvorite od profesora Amera docker kontejner ;)


## Prerequisite dependancies

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
