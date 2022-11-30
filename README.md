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
