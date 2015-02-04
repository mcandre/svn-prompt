# bash/zsh svn prompt support

# EXAMPLE

```
$ cd mycoolsvnrepo/
mycoolsvnrepo$ cd trunk/src/main/java/
java (trunk)$ cd ../branches/feature-1/src/main/java/
java (feature-1)$
```

# INSTALL

Download `svn-prompt.sh`:

```
$ wget -O ~/svn-prompt.sh https://raw.githubusercontent.com/mcandre/svn-prompt/master/svn-prompt.sh
```

Then configure your `PS1` shell variable to use svn-prompt:

```
# svn prompt
# See https://raw.githubusercontent.com/mcandre/svn-prompt/master/svn-prompt.sh
. $HOME/svn-prompt.sh

export PS1='\W$(parse_svn_branch)$ '
```

Or, if you would like to combine [git prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh) with svn prompt:

```
# git prompt
# See https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh
. $HOME/git-prompt.sh

# svn prompt
# See https://raw.githubusercontent.com/mcandre/svn-prompt/master/svn-prompt.sh
. $HOME/svn-prompt.sh

export PS1='\W$(__git_ps1 " (%s)")$(parse_svn_branch)$ '
```

Then update your shell:

```
$ source ~/.bash_profile
```

Now `cd` around a Subversion repository to test your new shell prompt!
