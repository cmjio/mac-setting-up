# Installing MacVim

Download MacVim from this link: [Google Code > Project > MacVim](http://code.google.com/p/macvim/)<br />
Then simply drag that to your applications folder, remember to install the `mvim` script to your location of preference.

# Setting up Vim

I have my settings linked up with DropBox, so I would use the following commands. If you want to have my settings follow this repo: [GitHub > Greduan/dotfiles > vim](https://github.com/Greduan/dotfiles/tree/master/vim)

`ln -s ~/Dropbox/dotfiles/vim ~/.vim`<br />
`ln -s ~/Dropbox/dotfiles/vim/vimrc ~/.vimrc`

# Configurin Git to use mvim

Simply run the following command in the Terminal:

`git config --global core.editor "mvim -f"`
