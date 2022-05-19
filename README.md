//Prerequisite DEPENDANCIES - install using pacman preferrably


sudo pacman -S nodejs
  --//--       Yarn
  --//--       Clang
  --//--     python-pip
pip install pynvim

# nvim
Neovim Configuration for c++

--Installation guide--

1.Open terminal and install the latest neovim version 
sudo pacman -S neovim

2. Go to ~/.config and create a dir called nvim

3.In the nvim dir create a init.vim file and copy everything from the init.vim file from my repo.

4.In the terminal type
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
5.Go back to the init.vim while and while in Command mode type :PlugInstall

6.Go to ~/.local/share/nvim/plugged/coc.nvim and in that dir type "yarn install"

7. In the nvim.init file in COmmand mode type 
CocInstall coc-clangd then CocInstall coc-snippets
