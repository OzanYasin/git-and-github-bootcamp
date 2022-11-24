# Undo Changes

## Checkout

The `git checkout` command is like a Git Swiss Army knife.
Many developers think it is overloaded, which is what lead to the addition of the git switch and git restore commands

We can use **checkout** to create branches, switch to new branches, restore files, and undo history!

We can use `git checkout <commit-hash>` to view a previous commit.

Remember, you can use the `git log` command to view commit hashes. We just need the **first 7 digits** of a commit hash.

Don't panic when you see the following message...

## Detached HEAD?!

"You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any commits you make in this state without impacting any branches by switching back to a branch."

- HEAD is a pointer to the current branch reference
- The branch reference is a pointer to the last commit made on a particular branch

> When we checkout a particular commit, **HEAD points at that commit** rather than at the branch pointer.

### You have a couple options:

1.  Stay in detached HEAD to examine the contents of the old commit. Poke around, view the files, etc.
2.  Leave and go back to wherever you were before - reattach the HEAD
3.  Create a new branch and switch to it. You can now make and save changes, since HEAD is no longer detached.

∆ `git checkout` supports a slightly odd syntax for referencing previous commits relative to a particular commit.

**HEAD~1** refers to the commit before HEAD (parent)

**HEAD~2** refers to 2 commits before HEAD (grandparent)
