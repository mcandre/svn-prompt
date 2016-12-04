# bash/zsh svn prompt support

# EXAMPLE

```
$ cd mycoolsvnrepo/
mycoolsvnrepo$ cd trunk/src/main/java/
java (trunk)$ cd ../branches/feature-1/src/main/java/
java (feature-1)$
```

# INSTALL

Download [svn-prompt.sh](https://raw.githubusercontent.com/mcandre/svn-prompt/master/lib/svn-prompt.sh) and place into `$HOME`:

```
$ wget -O $HOME/svn-prompt.sh https://raw.githubusercontent.com/mcandre/svn-prompt/master/lib/svn-prompt.sh
```

Then configure your `$HOME/.bash_profile` or similar shell configuration to use svn-prompt:

```
# svn prompt
# See https://raw.githubusercontent.com/mcandre/svn-prompt/master/lib/svn-prompt.sh
. $HOME/svn-prompt.sh

export PS1='\W$(parse_svn_branch)$ '
```

If you would like to use svn prompt with [git prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh):

```
# git prompt
# See https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh
. $HOME/git-prompt.sh

# svn prompt
# See https://raw.githubusercontent.com/mcandre/svn-prompt/master/lib/svn-prompt.sh
. $HOME/svn-prompt.sh

export PS1='\W$(__git_ps1 " (%s)")$(parse_svn_branch)$ '
```

Then update your shell:

```
$ source $HOME/.bash_profile
```

Now `cd` around a Subversion repository to test your new shell prompt!

# CREDITS

Inspired by [git prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh) and [hocuspokus](http://hocuspokus.net/2009/07/add-git-and-svn-branch-to-bash-prompt/).
