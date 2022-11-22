# Comparing Changes with Git Diff

Documents: https://git-scm.com/docs/git-diff

## Git Diff

We can use the `git diff` command to view changes between commits, branches, files, our working directory, and more!

We often use `git diff` alongside commands like `git status` and `git log`, to get a better picture of a repository and how it has changed over time.

Without additional options, `git diff` lists all the changes in our working directory that are NOT staged for the next commit.

`git diff HEAD` lists all changes in the working tree since your last commit.

`git diff --staged` or `git diff --cached` will list the changes between the staging area and our last commit.

## Diff-ing Specific Files

You can view the changes within a specific file by using `git diff <filename>`.
