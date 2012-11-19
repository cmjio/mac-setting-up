# Random configurations

This section will contain some random tips for customizing your shell command prompt etc.

These lines of code will simply enable colors in your ls, and other things, these are for Mac OSX, Linux may be different:

    # Enabling colors for everything, also allows you to use them in prompt
    autoload -U colors && colors

## Setting aliases

This line of code will make sure that `ls` always displays stuff with the following options, I suggest you use them as they are *very* useful:

    # Making sure that ls always uses these settings, even when not specified
    alias ls="ls -la -Gp -F"

## History settings

The following options will customize the `history` command a little bit:

    # Set history options
    HISTSIZE=1000
    SAVEHIST=1000
    HISTFILE=~/.history
    export HIST_IGNORE_ALL_DUPS

## Prompt

These options do what the comments say, this is pretty much, only for the Git status BTW:

    # Autoload zsh functions
    fpath=(~/.zsh/functions $fpath)
    autoload -U ~/.zsh/functions/*(:t)
    
    # Enable auto-execution of functions
    typeset -ga preexec_functions
    typeset -ga precmd_functions
    typeset -ga chpwd_functions

These options are very important for the prompt and Git:

    # Append git functions needed for prompt
    preexec_functions+='preexec_update_git_vars'
    precmd_functions+='precmd_update_git_vars'
    chpwd_functions+='chpwd_update_git_vars'

The following is my current prompt:

    # Set the prompt
    PROMPT=$'%{${fg[yellow]}%}[%T] %{${fg[cyan]}%}%~$(prompt_git_info)%{${fg[default]}%} >>> '
    # Set the right side of my prompt
    RPROMPT=$'%{${fg[default]}%}[%n@%m]'
