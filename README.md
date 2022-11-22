# Working With Branches

On large projects, we often work in multiple contexts:

1. You're working on 2 different color scheme variations for your website at the same time, unsure of which you like best
2. You're also trying to fix a horrible bug, but it's proving tough to solve. You need to really hunt around and toggle some code on and off to figure it out.
3. A teammate is also working on adding a new chat widget to present at the next meeting. It's unclear if your company will end up using it.
4. Another coworker is updating the search bar autocomplete.
5. Another developer is doing an experimental radical design overhaul of the entire layout to present next month.

## **Branches**

Branches are an essential part of Git!

Think of branches as alternative timelines for a project.

They enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.

If we make changes on one branch, they do not impact the other branches (unless we merge the changes)

## **Master**

Many people designate the master branch as their "source of truth" or the "official branch" for their codebase, but that is left to you to decide.

From Git's perspective, the master branch is just like any other branch. It does not have to hold the "master copy" of your project.

## **Head**

We'll often come across the term HEAD in Git.

HEAD is simply a pointer that refers to the current "location" in your repository. It points to a particular branch reference.

So far, HEAD always points to the latest commit you made on the master branch, but soon we'll see that we can move around and HEAD will change!

## **View Branches**

Use `git branch` to view your existing branches. The default branch in every git repo is master, though you can configure this.

Look for the \* which indicates the branch you are currently on.

## **Creating Branches**

Use `git branch <branch-name>` to make a new branch based upon the current HEAD

This just creates the branch. It does not switch you to that branch (the HEAD stays the same)

## **Switching Branches**

Once you have created a new branch,
use `git switch <branch-name>` to switch to it.

## **Another Way of Switching**

Historically, we used `git checkout <branch-name>` to switch branches. This still works.

The checkout command does a million additional things, so the decision was made to add a standalone switch command which is much simpler.

You will see older tutorials and docs using checkout rather than switch. Both now work.

## **Creating & Switching**

Use git switch with the -c flag to create a new branch AND switch to it all in one go.

Remember -c as short for "create"

> When you switch branches, if you have unstaged changes, they will come with you; if they're in conflict, git will yell at you.

## **Deleting & Renaming Branches**

With `git -d <branchname>` branch will be deleted. You may specify more than one branch for deletion. If the branch currently has a reflog then the reflog will also be deleted.

`git -D <branchname>` is shortcut for `--delete --force`.

> To delete a branch you had to go anywhere else but that branch, you could not delete from the branch; but to rename you have to be on the branch that you work on.

## **Viewing More Info**

Use the `git branch -v` command to view more information about each branch.
