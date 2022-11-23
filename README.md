# Stashing

"I'm not at all ready to commit these changes, but I also don't want to take them with me to master..."

Git provides an easy way of stashing these uncommitted changes so that we can return to them later, without having to make unnecessary commits.

## Stash Save

`git stash` is super useful command that helps you save changes that you are not yet ready to commit. You can stash changes and then come back to them later.

Running `git stash` will take all uncommitted changes (staged and unstaged) and stash them, reverting the changes in your working copy.

> You can also use `git stash save` instead.

## Stash Pop

Use `git stash pop` to remove the most recently stashed changes in your stash and re-apply them to your working copy.

## Stash Apply

You can use `git stash apply` to apply whatever is stashed away, without removing it from the stash. This can be useful if you want to apply stashed changes to multiple branches.

## Untracked Files

If you have untracked files (files that you have never checked in to Git), they will not be included in the stash.

Fortunately, you can use the -u option to tell git stash to include those untracked files.

## Stashing Multiple Times

You can add multiple stashes onto the stack of stashes. They will all be stashed in the order you added them.

## Viewing Stashes

You can run `git stash list` command to view all stashes.

> Stash ID's look like `stash@{0}, stash@{1}, stash@{2}...`
