# Terminal setup

Set up the Terminal application (command line) to use theme of my preference... My own:<br />
[FileSwap.com > Eduan > Eduan.terminal](http://www.fileswap.com/dl/t0wJEala52/Eduan.terminal.html)<br />
[FileSwap.com > Eduan > Eduan Solarized.terminal](http://www.fileswap.com/dl/RF0JsEODz/Eduan_Solarized.terminal.html)

## Setting up some settings

`$ touch ~/.zshrc`<br />

`$ mvim ~/.zshrc`

    alias ls="ls -la -Gp -F"

# Git Setup

## Installing Git

1. Go to [Git-scm.com](http://git-scm.com/) and download the latest version of Git.
2. Install it.

## Configuring Git

Do the following in the command line:

`$ touch ~/.gitmessage.txt`<br />
`$ mvim ~/.gitmessage.txt`

    Short (50 chars or less) summary of changes.

    More detailed explanatory text. Wrap it to about 72 chars. You can of
    course use multiple lines, as long as no line is longer than 72 chars.

    * For something you fixed, like a bug a glitch or something
    + For something new you added, be it a class, function, or whole feature
    ~ If you changed something, be it text, a function, etc.
    - If you removed something
    +~ If you improved something in some or any way

                                       50 chars mark |       72 chars mark |

To have the most recent version of my .gitmessage.txt file simply visit the followng Gist:<br />
[gist: 3981302](https://gist.github.com/3981302)

`$ git config --global user.name "Eduan Lavaque"`<br />
`$ git config --global user.email "eduan@snapsimpletech.com"`

`$ git config --global core.editor "mvim -f"`<br />
`$ git config --global color.ui true`<br />
`$ git config --global commit.template ~/.gitmessage.txt`<br />
`$ git config --global core.autocrlf input`

`git config --global alias.logg "log --graph --decorate --oneline --all --abbrev-commit"`

## Adding auto completion and showing current branch

In order to have Zsh show your current branch, and show it's status, you need to follow the instructions in this blog post: [SebastianCelis.com > Zsh Prompt for Git Users](http://sebastiancelis.com/2009/11/16/zsh-prompt-git-users/)

## Password caching

In order for Git to not ask for your password every time you push a change to an online repo, follow the instructions in this help article by GitHub in order to setup the `osxkeychain` application: [GitHub:Help > Setup Git > Password Caching](https://help.github.com/articles/set-up-git#password-caching)
