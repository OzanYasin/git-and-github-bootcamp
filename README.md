# Git & GitHub Bootcamp by Colt Steele

All Git Commands: https://git-scm.com/docs

## Commits in Details

### **Atomic Commits**

When possible, a commit should encompass a single feature, change, or fix. In other words, try to keep each commit focused on a single thing.

This makes it much easier to undo or rollback changes later on. It also makes your code or project easier to review.

### **Present-Tense Imperative Style**

Describe your changes in imperative mood, e.g. "make xyzzy do frotz" instead of "[This patch] makes xyzzy do frotz" or "I changed xyzzy to do frotz", as if you are giving orders to the codebase to change its behavior.

Blog Post About That:
https://medium.com/@corrodedlotus/which-tense-should-be-used-on-a-git-commit-message-121cb641134b

> First line of the commit should be the summary of the commit message (if there is more on detail about the commit).

`git log --oneline` shows the commit logs with only first line.

**! You do NOT have to follow this pattern**

Though the Git docs suggest using present-tense imperative messages, many developers prefer to use past-tense messages. All that matters is consistency, especially when working on a team with many people making commits

### **Changing The Editor**

Git Configuration Docs:
https://git-scm.com/book/en/v2/Appendix-C%3A-Git-Commands-Setup-and-Config

`git config --global core.editor "code --wait"`

By doing that, vscode is the new committing text editor instead of Vim (default text editor).

### **Amending Commits**

Suppose you just made a commit and then realized you forgot to include a file! Or, maybe you made a typo in the commit message that you want to correct.

Rather than making a brand new separate commit, you can "redo" the previous commit using
the --amend option

### **Ignoring Files**

We can tell Git which files and directories to ignore in a given repository, using a .gitignore file.
This is useful for files you know you NEVER want to commit, including:

- Secrets, API keys, credentials, etc.
- Operating System files (.DS_Store on Mac)
- Log files
- Dependencies & packages

### **.gitignore**

Create a file called **.gitignore** in the root of a repository. Inside the file, we can write patterns to tell Git which files & folders to ignore:

- `.DS_Store` will ignore files named .DS_Store
- `folderName/` will ignore an entire directory
- `*.log` will ignore any files with the .log extension

GitIgnore Docs: https://git-scm.com/docs/gitignore

> Recommended starting place for your project: https://www.toptal.com/developers/gitignore/

## Working With Branches

On large projects, we often work in multiple contexts:

1. You're working on 2 different color scheme variations for your website at the same time, unsure of which you like best
2. You're also trying to fix a horrible bug, but it's proving tough to solve. You need to really hunt around and toggle some code on and off to figure it out.
3. A teammate is also working on adding a new chat widget to present at the next meeting. It's unclear if your company will end up using it.
4. Another coworker is updating the search bar autocomplete.
5. Another developer is doing an experimental radical design overhaul of the entire layout to present next month.

### **Branches**

Branches are an essential part of Git!

Think of branches as alternative timelines for a project.

They enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.

If we make changes on one branch, they do not impact the other branches (unless we merge the changes)

### **Master**

Many people designate the master branch as their "source of truth" or the "official branch" for their codebase, but that is left to you to decide.

From Git's perspective, the master branch is just like any other branch. It does not have to hold the "master copy" of your project.

### **Head**

We'll often come across the term HEAD in Git.

HEAD is simply a pointer that refers to the current "location" in your repository. It points to a particular branch reference.

So far, HEAD always points to the latest commit you made on the master branch, but soon we'll see that we can move around and HEAD will change!
