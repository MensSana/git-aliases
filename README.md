# git helpers
This is what we use in our Cygwin MinTTY console.<br/>
This should work as-is in most bash environments.

## aliases

##### gitconfig
    [alias]
      history = show --pretty=format:'%n%C(red)%h%C(reset)%C(yellow)%d %C(cyan)%cr%C(reset) par %C(bold green)%an%C(reset)%n%C(bold white)%B%C(white)' --abbrev-commit --name-status

## shell prompt

##### bash.bashrc
    . /etc/gitprompt
    export PS1="\$(__git_ps1)\n${PS1}"    

    
