# bash/zsh svn prompt support

# EXAMPLE

```
$ cd mycoolsvnrepo/
mycoolsvnrepo$ cd trunk/src/main/java/
java (trunk)$ cd ../branches/feature-1/src/main/java/
java (feature-1)$
```

# INSTALL

Download `svn-prompt.sh`.

Then add:

```
export PS1='\W$(parse_svn_branch)$ '
```

Or, if you would like to combine [git prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh) with svn prompt, add:

```
export PS1='\W$(__git_ps1 " (%s)")$(parse_svn_branch)$ '
```

Update your shell:

```
$ source ~/.bash_profile
```

Now `cd` around a Subversion repository to test your new shell prompt!
