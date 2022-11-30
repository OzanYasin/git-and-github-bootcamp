# Fetching and Pulling

## What is origin/master?

This is a "Remote Tracking Branch". It's a reference to the state of the master branch on the remote. I can't move this myself. It's like a bookmark pointing to the last known commit on the master branch on origin.

## Remote Tracking Branches

"At the time you last communicated with this remote repository, here is where x branch was pointing".

They follow this pattern `<remote>/<branch>`.

- **origin/master** references the state of the master branch on the remote repo named origin.
- **upstream/logoRedesign** references the state of the logoRedesign branch on the remote named upstream (a common remote name)

## Remote Branches

Run `git branch -r` to view the remote branches our local repository knows about.

> You can run `git status` to see if your branch is update, ahead or behind of origin/master.

Once you've cloned a repository, we have all the data and Git history for the project at that moment in time. However, that does not mean it's all in my workspace!

The github repo has a branch called cats, but when I run git branch I don't see it on my machine! All I see is the master branch. What's going on?

∆ By default, master branch is already tracking origin/master.

### _I want to work on a cats branch locally!_

I could checkout origin/cats, but that puts me in detached HEAD.

I want my own local branch called cats, and I want it to be connected to origin/cats, just like my local master branch is connected to origin/master.

### _It's super easy!_

Run `git switch <remote-branch-name>` to create a new local branch from the remote branch of the same name.

`git switch cats` makes me a local cats branch AND sets it up to track the remote branch origin/cats.

> The new `command git switch` makes this super easy to do! It used to be slightly more complicated using `git checkout` **(git checkout --track origin/master)**.

## Fetching

Fetching allows us to download changes from a remote repository, BUT those changes will not be automatically integrated into our working files.

It lets you see what others have been working on, without having to merge those changes into your local repo.

Think of it as "please go and get the latest information from Github, but don't screw up my working directory."

## Git Fetch

The `git fetch <remote>` command fetches branches and history from a specific remote repository. It only updates remote tracking branches.

`git fetch origin` would fetch all changes from the origin remote repository.

> If not specified, `<remote>` defaults to origin.

We can also fetch a specific branch from a remote using `git fetch <remote> <branch>`

For example, `git fetch origin master` would retrieve the latest information from the master branch on the origin remote repository.

## Pulling

`git pull` is another command we can use to retrieve changes from a remote repository. Unlike fetch, pull actually updates our HEAD branch with whatever changes are retrieved from the remote.

_"Go and download data from Github AND immediately update my local repo with those changes."_

> **git pull = git fetch + git merge**

## Git Pull

To pull, we specify the particular remote and branch we want to pull using `git pull <remote> <branch>`. Just like with git merge, it matters WHERE we run this command from. Whatever branch we run it from is where the changes will be merged into.

`git pull origin master` would fetch the latest information from the origin's master branch and merge those changes into our current branch.
