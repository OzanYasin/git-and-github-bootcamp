# Merging Branches

Documents: https://git-scm.com/docs/git-merge

Branching makes it super easy to work within self-contained contexts, but often we want to incorporate changes from one branch into another!

We can do this using the `git merge` command

## **Merging**

The merge command can sometimes confuse students early on. Remember these two merging concepts:

- We merge branches, not specific commits
- We always merge to the current HEAD branch

## **Merging Made Easy**

To merge, follow these basic steps:

1. Switch to or checkout the branch you want to merge the changes into (the receiving branch)
2. Use the git merge command to merge changes from a specific branch into the current branch.

## **Conflicts!**

Depending on the specific changes your are trying to merge, Git may not be able to automatically merge. This results in **merge conflicts**, which you need to manually resolve.

- When you encounter a merge conflict, Git warns you in the console that it could not automatically merge.

> It also changes the contents of your files to indicate the conflicts that it wants you to resolve.

## **Conflict Markers**

The content from your current HEAD (the branch you are trying to merge content into) is displayed between the **<<<<<<< HEAD** and **=======**

&&

The content from the branch you are trying to merge from is displayed between the **=======** and **>>>>>>>** symbols.

## **Resolving Conflicts**

Whenever you encounter merge conflicts, follow these steps to resolve them:

1. Open up the file(s) with merge conflicts
2. Edit the file(s) to remove the conflicts. Decide which branch's content you want to keep in each 3. conflict. Or keep the content from both.
3. Remove the conflict "markers" in the document
4. Add your changes and then make a commit!
