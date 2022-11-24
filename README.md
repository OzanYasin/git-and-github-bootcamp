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
