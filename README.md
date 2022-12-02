# Git Behind The Scenes: Hashing & Objects

In **.git** folder, there is objects and refs folder, config, HEAD, index files and more...

Documents: https://git-scm.com/docs/git-config

## Config

The config file is for...configuration. As we know, there is a way to configure global settings like our name and email across all Git repos, but we can also configure things on a per-repo basis.

## Refs Folder

Inside of refs, you'll find a heads directory. **_refs/heads_** contains one file per branch in a repository. Each file is named after a branch and contains the hash of the commit at the tip of the branch.

For example **refs/heads/master** contains the commit hash of the last commit on the master branch.

Refs also contains a **refs/tags** folder which contains one file for each tag in the repo.

## HEAD

HEAD is just a text file that keeps track of where HEAD points.

> If it contains refs/heads/master, this means that HEAD is pointing to the master branch.

In detached HEAD, the HEAD file contains a commit hash instead of a branch reference
