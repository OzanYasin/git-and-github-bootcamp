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
