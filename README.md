# Homer v1.2

Your `$HOME` needs **Homer** :)

**Homer** manages your dotfiles and folders using just `git`. No symlink is involved!
What makes **Homer** different is:

+ works directly in the $HOME
+ keeps tracking of added files, ignoring everythig else
+ fully tracks all added folders (!)

In other words, you pick files and folders from your `$HOME` and add it to your **Homer**. Everything else is ignored, which is very convenient when used in `$HOME`. **Homer** treats added files and folders differently:

+ files are simply tracked when they are added.
+ folders, hover, are fully synchronized! There is no need to add manually each new file from a folder. **Homer** will do all that. Of course, you can use `.gitignore` in the folders to simply ignore some files. This makes everyday-life much easier!

## Installation :gift:

Download `homer` to your `$PATH` or current folder. Done!

## Usage

### Setup :clapper:

First you need to _initialize_ **Homer** and connect to GitHub by passing `user/repo_name`:

```shell
homer init github-user/homer-repo
```

If you have another machine, just _clone_ **Homer** from the GitHub:

```shell
homer clone github-user/homer-repo
```

### Every-day work :tophat:

Anytime you can check the _status_ of what is going on; what is new, changed deleted or untracked:

```shell
homer status
```

Start _adding_ files and folders. When folder is added, all its files are added as well!
Use `.gitgnore` to ignore files.

```shell
homer add .zsh
homer add bin
...
```

If you already have some folders included in **Home**, you can simply add all untracked files bellonging to included folders with simple:

```shell
homer add
```

Finally, _put_ all your changes to the repo (this command will also add all untracked files from included folders):

```shell
homer put
```

On the another computer, _get_ the changes:

```shell
homer get
```

### Reset and Remove :warning:

To reset some file:

```shell
homer reset bin/text.txt
```

You can reset all changes with:

```shell
homer reset
```

To remove single file from the repo:

```shell
homer remove <FILE>
```

## Use with ❤

Do it!
