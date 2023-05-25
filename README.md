# dotfiles
1. Run these commands
```sh
git clone git@github.com:iserh/dotfiles.git ~/dotfiles
ln -s ~/dotfiles/.tmux.conf ~/.tmux.conf
ln -s ~/dotfiles/.vimrc ~/.vimrc
ln -s ~/dotfiles/.editorconfig ~/.editorconfig
```

## Vim
If not already done you also have to install Vundle
```sh
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

Go into a vim session and type `:PluginInstall`


## Tmux
Install tpm
```sh
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Then go into a tmux session and type `C-a I`


## GNOME terminal
This section is following the instructions on https://github.com/0xcomposure/monokai-gnome-terminal:

You need the dconf command (if you run a recent Gnome version).
```sh
sudo apt-get install dconf-cli
```

```sh
git clone https://github.com/0xComposure/monokai-gnome-terminal
./monokai-gnome-terminal/install.sh
rm -rf monokai-gnome-terminal
```


## Apple terminal
Make sure your on `osx` branch of this repo. After installing vim plugins run the following command to match the terminal background:
```sh
~/dotfiles/monokai_background.sh
```


## Oh-my-zsh
Run the following command to install oh-my-zsh and setup the default `.zshrc`:
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
cp ~/dotfiles/.zshrc_default ~/.zshrc
cp -r ~/dotfiles/conda-zsh-completion ~/.oh-my-zsh/custom/plugins/conda-zsh-completion
```


## Jupyter
Using `jupyterthemes` like on https://medium.com/@rbmsingh/making-jupyter-dark-mode-great-5adaedd814db. Run
```sh
pip install jupyterthemes
jt -t grade3 -fs 100 -tfs 12 -nfs 115 -cellw 95% -T
```
```sh
# for dark theme
jt -t monokai -fs 100 -tfs 12 -nfs 115 -cellw 95% -T
```

## justfile for python
```sh
ln -s ~/dotfiles/python/justfile ~/dev/justfile
```
