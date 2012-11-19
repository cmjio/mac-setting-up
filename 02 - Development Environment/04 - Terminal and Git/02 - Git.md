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

First make sure that you don't already have this functionality. Run the following command:<br />
`$ git osxkeychain`

You probably don't have it at this point, so do the following commands:<br />
`$ curl -s -O http://github-media-downloads.s3.amazonaws.com/osx/git-credential-osxkeychain`<br />
`$ chmod u+x git-credential-osxkeychain`

Now you need to find out where Git is installed:<br />
`$ which git`<br />
`$ sudo mv git-credential-osxkeychain [results/given/in/the/previous/command]`

Now configure Git to make sure it uses it:<br />
`$ git config --global credential.helper osxkeychain`

And you're done!

## Installing hub

To install hub simply follow the instructions in this web-page (as there is more than 1 way to do it): http://defunkt.io/hub/

Here's `hub`'s repo BTW: [GitHub > defunkt/hub](https://github.com/defunkt/hub)

### What is hub?

hub is a neat little utility that allows you to work better and easier with GitHub.

If you use GitHub, then you *need* hub.

### Setting up alias

`$ mvim ~/.zshrc`

    alias git="hub"

\* This step is optional, but *very*, *very* recommended.
