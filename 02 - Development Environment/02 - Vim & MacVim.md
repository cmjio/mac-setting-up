## Getting MacVim

To get MacVim, simply go to [Google Code > Project > MacVim](http://code.google.com/p/macvim/) and download the latest version. Or go to [GitHub > b4winckler/macvim > Wiki > ChangeLog](https://github.com/b4winckler/macvim/wiki/ChangeLog) which will contain the latest download, and a changelog.

## Installing MacVim

Simply decompress the downloaded file, drag the MacVim application to the Applications folder, and then simply move the `mvim` shell script to your preferred location for personal scripts and stuff. Mine is `usr/local/bin`.

## Setting it up

In order to get the latest version of my `.vimrc` file and others, simply go to my repo ([GitHub > Greduan/dotfiles > vim](https://github.com/Greduan/dotfiles/tree/master/vim)) and you can download them there. Then you would simply run the following commands:

`$ ln -s [path\ to\ vim\ folder] ~/.vim`<br />
`$ ln -s [path\ to\ vimrc] ~/.vimrc`

In my case it would be:

`$ ln -s ~/Dropbox/dotfiles/vim ~/.vim`<br />
`$ ln -s ~/Dropbox/dotfiles/vim/vimrc ~/.vimrc`

This would ensure that you have the latest version of my configuration files, remember it's a repo, so you can sync it to my repo whenever you want.
