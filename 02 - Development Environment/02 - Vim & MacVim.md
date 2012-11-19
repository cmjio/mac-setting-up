## Getting MacVim

To get MacVim, simply go to [Google Code > Project > MacVim](http://code.google.com/p/macvim/) and download the latest version. Or go to [GitHub > b4winckler/macvim > Wiki > ChangeLog](https://github.com/b4winckler/macvim/wiki/ChangeLog) which will contain the latest download, and a changelog.

## Installing MacVim

Simply decompress the downloaded file, drag the MacVim application to the Applications folder, and then simply move the `mvim` shell script to your preferred location for personal scripts and stuff. Mine is `usr/local/bin`.

## Setting it up

In order to get the latest version of my `.vimrc` file and others, simply go to my repo ([GitHub > Greduan/dotfiles > vim](https://github.com/Greduan/dotfiles/tree/master/vim)) and you can download them there. Then you would simply run the following commands:

`$ ln -s [path\ to\ vim\ folder] ~/.vim`<br />
`$ ln -s [path\ to\ vimrc] ~/.vimrc`<br />
`$ ln -s [path\ to\ gvimrc] ~/.gvimrc`

In my case it would be:

`$ ln -s ~/.dotfiles/vim ~/.vim`<br />
`$ ln -s ~/.dotfiles/vim/vimrc ~/.vimrc`<br />
`$ ln -s ~/.dotfiles/vim/gvimrc ~/.gvimrc`

This would ensure that you have the latest version of my configuration files, remember it's a repo, so you can sync it to my repo whenever you want.

## Avoiding Python errors

If you get the following errors when you try to run `vim` in the Terminal:

    Traceback (most recent call last):
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site.py", line 565, in <module>
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site.py", line 547, in main
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site.py", line 278, in addusersitepackages
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site.py", line 253, in getusersitepackages
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site.py", line 243, in getuserbase
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/sysconfig.py", line 523, in get_config_var
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/sysconfig.py", line 419, in get_config_vars
      File "/System/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/sysconfig.py", line 298, in _init_posix
    IOError: invalid Python installation: unable to open /usr/include/python2.7/pyconfig.h (No such file or directory)

Then you need to run the following commands in the Terminal:<br />
`$ sudo mkdir -p /usr/include/python2.7`
`$ sudo ln -s /System/Library/Frameworks/Python.framework/Versions/Current/include/python2.7/pyconfig.h /usr/include/python2.7/pyconfig.h`
