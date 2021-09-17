# Ubuntu Installations

## Step 1: Install vim with +python 

`` sudo apt install vim-gtk vim-nox ``

## Step 2: Install Dotfiles

1) Add git and nodejs, cmdtest for coc.nvim

`` sudo apt install git nodejs cmdtest npm ctags fzf ``

2) Clone dotfiles

`` git clone https://github.com/yukikongju/dotfiles ``

3) generate symlinks for .vim, snippets, bashrc, tmux.conf

```
./dotfiles/scripts/vim.sh 
./dotfiles/scripts/snippets.sh 

```

4) Install Vim Plug for Linux

```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim' 
```
       
5) Install Pluggins inside vim with `` :PlugInstall``

6) Activate coc.nvim by going into coc.vim directory and yarn install

```
cd .vim/plugged/coc.nvim
yarn install
```

If error, see `` :CocInfo `` to debug


## Step 3: Install tmux

`` sudo install tmux ``

## Step 4: Install Latex Compiler and viewer

1) Install pdflatex Compiler

`` sudo apt install texlive-latex-base latexmk evince ``

2) Install Extra latex packages

`` sudo apt install texlive-latex-extra texlive-bibtex-extra``

## Step 5: Install Python 

`` sudo apt install python3-pip ``

## Step 6: Install Vimwiki

1) Install :VimWiki2HTML

`` pip install vimwiki-markdown``

2) Install Ruby so that vimwiki-markdown can compile

`` sudo apt-get install ruby-full``

## Step 7: Install fuzzy finder

`` sudo install ripgrep the-silver-searcher ``


### TODOs

- [ ] Vimwiki2HTML doesn't work
- [ ] 

