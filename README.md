## Aliases

##### gitconfig
    [alias]
      history = show --pretty=format:'%n%C(red)%h%C(reset)%C(yellow)%d %C(cyan)%cr%C(reset) par %C(bold green)%an%C(reset)%n%C(bold white)%B%C(white)' --abbrev-commit --name-status

## Prompt

##### bash.bashrc
    . /etc/gitprompt
    export PS1="\$(__git_ps1)\n${PS1}"    

    
