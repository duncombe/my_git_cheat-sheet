# My GIT Cheat Sheet

## Git commands

`git log --pretty=oneline --abbrev-commit <path>` 

short hand: `git log --oneline <path>`

`git log  --graph <path>`

Fix ANSI escape codes in `git log`: `git config --global core.pager "less -R"`

## Cheatsheets and Tutorials

- [Atlassian tutorials](https://www.atlassian.com/git/tutorials/)
- [NDP Interactive Cheat Sheet](http://ndpsoftware.com/git-cheatsheet.html)
- [Git Fix Um](http://sethrobertson.github.io/GitFixUm/fixup.html)
- [How to escape a git mess](http://justinhileman.info/article/git-pretty/git-pretty.png)
- [Think like a git](http://think-like-a-git.net/)
- [git ready](http://gitready.com/)

## Powershell Commands

|Powershell command| Unix equivalent|
|---|---|
| `get-help` | `man` |
| `remove-Item` | `rm` |
| `remove-Item -recurse -force ` | ` rm -rf ` |


## Python Wisdom

[Do not use --pylab flag for iPython](http://nbviewer.ipython.org/github/Carreau/posts/blob/master/10-No-PyLab-Thanks.ipynb)   
When you need to see a notebook without re-executing, trust notebooks with     
``` ipython trust mynotebook.ipynb [other notebooks.ipynb]```   
to generate a new signature (git repositories?). [Explanation here](http://ipython.org/ipython-doc/dev/notebook/notebook.html).


## SSH problems?

This list from stackexchange solved a login problem on CdentOS :
- Your home directory `~`, your `~/.ssh` directory and the `~/.ssh/authorized_keys` file on the remote machine must be writable only by you: `rwx------` and `rwxr-xr-x` are fine, but `rwxrwx---` is no good,  even if you are the only user in your group (if you prefer numeric modes: 700 or 755, not 775).
If `~/.ssh` or `authorized_keys` is a symbolic link, the canonical path (with symbolic links expanded) is checked.
Your `~/.ssh/authorized_keys` file (on the remote machine) must be readable (at least 400), but you'll need it to be also writable (600) if you will add any more keys to it.
- Your private key file (on the local machine) must be readable and writable only by you: `rw-------`,`i.e. 600.
- Also, if SELinux is set to enforcing, you may need to run `restorecon -R -v ~/.ssh` (see e.g. Ubuntu bug 965663 and Debian bug report #658675; this is patched in CentOS 6 [*actually, no, it's not*]).

## Miscellaneous Stuff

- Kill a tree and print from Github? [Read this](https://gitprint.com/).  
- Install and use git as a non-root user? [Read this](http://joemaller.com/908/how-to-install-git-on-a-shared-host/).   
- Want a private or company Github-like server? [Read this about gitlab](https://about.gitlab.com/gitlab-ce/) or [this about gitorious](http://getgitorious.com/). 


![Tree killer](images/04142010inset2.jpg) 


