# Git And Github

# <u>WEEK 1</u>

## `diff` command

`diff` is used to find difference between two files.

## `diff -u` command

diff -u is used to compare two files, line by line, and have the differing lines compared side-by-side in the same output

## patch

Patch is useful for applying file differences. 

```shell
diff -u file1 file2 > file.patch
patch < file.patch 
```

## Setting up basic configurations

```shell
git config --global user.name "Name"
git config --global user.email "Email@email.com"
```

## `git init` command

Used to initiate a git repository.

## .git directory

Think of it as a database for your git project that stores the changes and the change history. It contains all the changes and their history.

## Working Tree

Working tree contains the current version of file.

## Staging Area

A file maintained by git that contains all of the information about what files and changes are going to go into your next commit.

## Untracked File

A file that is still to be added in staging area.

## `git add` command

Add a file or multiple files and folders in staging area.

## Commit

Explanation

Each time you make a commit, git records a new snapshot of the state of your project at that moment. Its a picture of exactly how all these files looked at certain moment in time.

## Files

Files in git can be of two type:

1. Tracked
2. Untracked

There can be three states of file:

1. Modified Files
2. Staged Files
3. Committed Files

## `git status` command

Gives the current status of our working tree.

## `git commit` command

Usage

```shell
git commit -m "Message"
```

## `git config -l` command

Lists the current configurations

## `git commit` `-a` tag

Used to add and commit modified file (Not new file) using a single command. 

## Writing Commit Message

This first line is a short summary of commit followed by a blank line. This is followed by a full description of changes.

Short Summary (50 Characters)

Full Description (72 Characters)

## `git log` command

Used to display us the history commits.



## <u>WEEK 2</u>

### `git commit` `-a` flag

This flag automatically stages every file that’s tracked and modified before doing the commit letting it skip the git add step.

`git commit -a` doesn’t work on new files because those are untracked.

Instead, git commit -a is a shortcut to stage any changes to tracked files and commit them in one step. 

### Head

Git uses the head alias to represent the currently checked out snapshot of your project. 

### `git log -p`

The p comes from patch, because using this flag gives us the patch that was created. 

### `git show <commit-id>`

This command takes a commit ID as a parameter, and will display the information about the commit and the associated patch

### `git log` `--stat` flag

This will cause git log to show some stats about the changes in the commit, like which files were changed and how many lines were added or removed. 

### `git diff`

Equivalent to `diff` command

`git diff` shows only unstaged changes by default.

### `git add` `-p` flag

When we use this flag, git will show us the change being added and ask us if we want to stage it or not. 

### `git diff` `--staged` flag

To see the `diff` on files that are staged but not commited.

### `git rm`

Remove a file from the git repository

Same as `rm` command in Linux.

### `git mv`

Used to rename or move file.

Same as `mv` command in Linux.

### .gitignore file

Inside this file, we'll specify rules to tell git which files to skip for the current repo. 

### `git checkout`

Usage

`git checkout <filename>`

think of it this way, you're checking out the original file from the latest storage snapshot. 

 we can use git checkout to revert changes to modify files before they get staged. 

But the file that need to be checkout is already have once added in git

### `git add *`

Add all files to the staging area

### `git reset`

If we realize we've added something to the staging area that we didn't actually want to commit, we can unstage our changes by using the git reset command. 

Usage

`git reset <COMMIT-ID> filename`

`git reset HEAD filename`

### `git commit --amend`

When we run git commit --amend, git will take whatever is currently in our staging area and run the git commit workflow to overwrite the previous commit. 

### `git revert`

So git revert will create a new commit, that is the opposite of everything in the given commit. 

`git revert HEAD`