# Homer

Your `$HOME` needs **Homer** :)

**Homer** manages your dotfiles and folders using just `git`. No symlink is involved!
What makes **Homer** different is:

+ works directly in the $HOME
+ keeps tracking of added files, ignoring everythig else
+ fully track all added folders (!)

In other words, you pick files and folders from your `$HOME`. **Homer** will ignore all other files and folders; however, it will fully synchronize the content of added folders! This difference makes everything super easy.

## Setup

First, initialize your local repo:

~~~ bash
cd ~
mkdir .homer
cd .homer
git init --bare
git config --local status.showUntrackedFiles no
alias homer='git --git-dir=$HOME/.homer/ --work-tree=$HOME'
~~~

This alias is just temporary, after the setup you will not longer need it.

Connect to Github repo:

~~~ bash
homer remote add origin https://github.com/<MYNAME>/<MYREPO>.git
homer push -u origin master
~~~

If you want to initialize an another machine, run this:

~~~ bash
cd ~
echo ".homer" >> .gitignore
alias homer='git --git-dir=$HOME/.homer/ --work-tree=$HOME'
git clone --bare https://github.com/<MYNAME>/<MYREPO>.git $HOME/.homer
homer config --local status.showUntrackedFiles no
homer checkout
~~~

## Usage

Download `homer` from this repo and put it on your `$PATH`. If everything is set,
you should be able to run it:

~~~ bash
homer
~~~

### Status

**Homer** status is just a nice, friendly overview of what is new, changed, deleted or untracked.

### Add

**Homer** can add all untracked files or specified. This step is not required.

### Put

**Homer** detects all the changes, new files etc.; commits everything and pushes to remote repo.

### Get

**Homer** checks if status is clean nad fetch all the changes from the remote repo.


## Use with ❤

Do it!