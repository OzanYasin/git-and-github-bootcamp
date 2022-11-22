# Comparing Changes with Git Diff

Documents: https://git-scm.com/docs/git-diff

## Git Diff

We can use the `git diff` command to view changes between commits, branches, files, our working directory, and more!

We often use `git diff` alongside commands like `git status` and `git log`, to get a better picture of a repository and how it has changed over time.

Without additional options, `git diff` lists all the changes in our working directory that are NOT staged for the next commit.

`git diff HEAD` lists all changes in the working tree since your last commit.
