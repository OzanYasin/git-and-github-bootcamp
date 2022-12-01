# Rebasing

There are two main ways to use the git rebase command:

- as an alternative to merging
- as a cleanup tool

> It's actually very useful, as long as you know when NOT to use it!

Documents: https://git-scm.com/docs/git-rebase

We can instead rebase the feature branch onto the master branch. This moves the entire feature branch so that it BEGINS at the tip of the master branch. All of the work is still there, but **we have re-written history.**

Instead of using a merge commit, rebasing rewrites history by **creating new commits** for each of the original feature branch commits.

### Why Rebase?

We get a much cleaner project history. No unnecessary merge commits! We end up with a linear project history.

## When Not to Rebase?

**Never** rebase commits that have been shared with others. If you have already pushed commits up to Github...DO NOT rebase them unless you are positive no one on the team is using those commits.

You do not want to rewrite any git history that other people already have. It's a pain to reconcile the alternate histories!

> In order to encounter a **conflict** while rebasing, you should resolve the conflict, add changed files and run `git rebase --continue` to finish rebasing safely. If you don't want to do that, you can abort rebasing by running `git rebase --abort`.

## Cleaning Up History With Interactive Rebase

Sometimes we want to **rewrite, delete, rename, or even reorder commits** (before sharing them)
We can do this using `git rebase`.
