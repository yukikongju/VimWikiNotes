# Vim Installations on Tablet using Termux

##### Step 0: Install Termux and f-Droid

##### Step 1: Install packages

```
pkg install vim-python tmux fzf git nodejs-lts yarn ctags texlive-bin ranger
```

##### Step 2: Install Plug Vim

```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

```

##### Step 3: Clone Dot Files and generate symbolic links

```
git clone https://github.com/yukikongju/dotfiles
./dotfiles/scripts/vim.sh
./dotfiles/scripts/snips.sh
```

##### Step 4: Activate coc.nvim

```
cd .vim/plugged/coc.nvim
yarn install
yarn build
```

##### Step 5: Remap Keyboard Key

For Fintie Keyboard:

##### Step 6: Make utils work

- VimWiki2HTML: `` pip install vimwiki-markdown ``
- pdflatex


##### Step 7: Git Authentification

```
git config --global user.email "<your_email@mail.com>"
git config --global user.name "<Your Name>"
git config --global credential.helper store
```

##### Step 8: Clone Repos

```
git clone https://github.com/yukikongju/VimWikiNotes
```

