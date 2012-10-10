# Terminal setup

Set up the Terminal application (command line) to use theme of my preference... My own: [FileSwap.com > Eduan > Eduan.terminal](http://www.fileswap.com/dl/t0wJEala52/Eduan.terminal.html)

## Setting up some settings

`$ touch ~/.bash_profile`<br />
`$ touch ~/.bashrc`<br />
`$ nano ~/.bash_profile`

    if [ -f ~/.bashrc ]; then
        source ~/.bashrc
    fi

`$ nano ~/.bashrc`

    export PS1='[\t] \w >>> '

# Git Setup

## Installing Git

1. Go to [Git-scm.com](http://git-scm.com/) and download the latest version of Git.
2. Install it.

## Configuring Git

Do the following in the command line:

`$ touch ~/.gitmessage.txt`<br />
`$ nano ~/.gitmessage.txt`

    Short (50 chars or less) summary of changes.

    More detailed explanatory text. Wrap it to about 72 chars.

    * For something you fixed, like a bug a glitch or something.
    + For something new you added, be it a class, function, or whole feature.
    ~ If you changed something, be it text, a function, etc.
    - If you removed something.

`$ git config --global user.name "Eduan Lavaque"`<br />
`$ git config --global user.email "eduan@snapsimpletech.com"`<br />

`$ git config --global core.editor "subl -n -w"`<br />
`$ git config --global color.ui true`<br />
`$ git config --global commit.template ~/.gitmessage.txt`<br />
`$ git config --global core.autocrlf input`

## Adding auto completion

`$ curl -OL https://github.com/git/git/raw/master/contrib/completion/git-completion.bash`<br />
`$ mv ~/git-completion.bash ~/.git-completion.bash`<br />
`$ nano .bashrc`

    if [ -f ~/.git-completion.bash ]; then
        source ~/.git-completion.bash
    fi