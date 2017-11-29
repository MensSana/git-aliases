# git helpers
This is what we use in our Cygwin MinTTY console.<br/>
This should work as-is in most bash environments.

## aliases

##### gitconfig
    [alias]
      history = show --pretty=format:'%n%C(red)%h%C(reset)%C(yellow)%d %C(cyan)%cr%C(reset) par %C(bold green)%an%C(reset)%n%C(bold white)%B%C(white)' --abbrev-commit --name-status

## shell prompt

#### Works with the following env variables:
    GIT_STATUS=0|1
    GIT_UNTRACKED=0|1

##### bash.bashrc
    . /etc/gitprompt
    __set_ps1()
    {
      . /etc/couleurs
      export PS1="\[$Rouge\][\[$BVert\]\u\[$Rouge\]@\[$BJaune\]\h\[$Rouge\]:\[$BCyan\]\W\[$Rouge\]]\n\[$Vert\]\$ \[$Normal\]"
      if test -z "$WINELOADERNOEXEC"
      then
        export PS1="\$(__git_ps1)\n${PS1}"
        export PS1="${PS1}"
      fi
    }
