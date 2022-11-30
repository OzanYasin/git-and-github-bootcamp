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

> `git checkout -` command will allow you to switch to the last branch you working on.

## Discarding Changes

Suppose you've made some changes to a file but don't want to keep them. To revert the file back to whatever it looked like when you last committed, you can use:

`git checkout HEAD <filename>` to discard any changes in that file, reverting back to the HEAD.

### Another Option

Rather than typing HEAD, you can substitute -- followed by the file(s) you want to restore.

`git checkout -- <filename>`

## Restore

`git restore` is a brand new Git command that helps with undoing operations.

Because it is so new, most of the existing Git tutorials and books do not mention it, but it is worth knowing!

Recall that `git checkout` does a million different things, which many git users find very confusing. `git restore` was introduced alongside `git switch` as alternatives to some of the uses for checkout.

## Unmodifying Files with Restore

Suppose you've made some changes to a file since your last commit. You've saved the file but then realize you definitely do NOT want those changes anymore!

To restore the file to the contents in the HEAD, use `git restore <file-name>`

`git restore <file-name>` restores using HEAD as the default source, but we can change that using
the **--source** option.

For example, `git restore --source HEAD~1 home.html` will restore the contents of **home.html** to its state from the commit prior to **HEAD.** You can also use a particular commit hash as the source.

## Unstaging Files with Restore

If you have accidentally added a file to your staging area with `git add` and you don't wish to include it in the next commit, you can use `git restore` to remove it from staging.

Use the **--staged** option like this: `git restore --staged <filename>`

> If you feel confused or forgot how to restore, `git status` reminds you what to use!

## Reset

Suppose you've just made a couple of commits on the master branch, but you actually meant to make them on a separate branch instead. To undo those commits, you can use `git reset`.

`git reset <commit-hash>` will reset the repo back to a specific commit. The commits are gone.

## Reset --hard

If you want to undo both the commits AND the actual changes in your files, you can use the **--hard** option.

for example, `git reset --hard HEAD~1` will delete the last commit and associated changes.

## Revert

`git revert` is similar to `git reset` in that they both **"undo"** changes, but they accomplish it in different ways.

`git reset` actually moves the branch pointer backwards, eliminating commits.

`git revert` instead creates a brand new commit which **reverses/undos** the changes from a commit. Because it results in a new commit, you will be prompted to enter a commit message.

## Should I Use Reset or Revert?

Both `git reset` and `git revert` help us reverse changes, but there is a significant difference when it comes to collaboration.

If you want to reverse some commits that other people already have on their machines, you should use **revert**.

If you want to reverse commits that you haven't shared with others, use **reset** and no one will ever know!

> Sometimes **reverting** a commit can result in conflicts, where you need to go into the file just like any other merge conflict and figure out what you want to keep and get rid of.
