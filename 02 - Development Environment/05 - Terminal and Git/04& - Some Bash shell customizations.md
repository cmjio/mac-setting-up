04 - Some Bash shell customizations.md

This section will contain some random tips for customizing your shell command prompt etc.

These lines of code will simply enable colors in your ls, and other things, these are for Mac OSX, Linux may be different:

    # Enabling colors for ls and others
    export CLICOLOR=true
    export LSCOLORS=exdxcxdxbxegedabagacad
    export GREP_OPTIONS='--color=auto'

This line of code will make sure that `ls` always displays stuff with the following options, I suggest you use them as they are *very* useful:

    # Making sure that ls always uses these settings, even when not specified
    alias ls="ls -la -Gp -F"

The following options will customize the `history` command a little bit:

    # Setting the format for the history command
    export HISTTIMEFORMAT='%b %d %I:%M %p '

    # Ignore the values ignoredups and ignorespace
    export HISTCONTROL=ignoreboth

    # Always ignore the following commands
    export HISTIGNORE="history:pwd:exit:df:ls:ls -la -Gp -F"
