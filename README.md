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

## Index

The index file is a binary file that contains a list of the files the repository is tracking. It stores the file names as well as some metadata for each file.

Not that the index does NOT store the actual contents of files. It only contains references to files.

## Objects Folder

The objects directory contains all the repo files. This is where Git stores the backups of files, the commits in a repo, and more.

The files are all compressed and encrypted, so they won't look like much!

> There is 4 type of Git Objects; commit, tree, blob, annotated and tag.

## Hashing Functions

Hashing functions are functions that map input data of some arbitrary size to fixed-size output values.

### **Cryptographic Hash Functions**

1.  One-way function which is infeasible to invert
2.  Small change in input yields large change in the output
3.  Deterministic - same input yields same output
4.  Unlikely to find 2 outputs with same value

### **SHA-1**

Git uses a hashing function called SHA-1 (though this is set to change eventually).

- SHA-1 always generates 40-digit hexadecimal numbers
- The commit hashes we've seen a million times are the output of SHA-1

## Git Database

Git is a **key-value data store.** We can insert any kind of content into a Git repository, and Git will hand us back a unique key we can later use to retrieve that content.

These keys that we get back are SHA-1 checksums.

## Hashing

The `git hash-object <file>` command takes some data, stores in in our .git/objects directory and gives us back the unique SHA-1 hash that refers to that data object.

In the simplest form, Git simply takes some content and returns the unique key that WOULD be used to store our object. But it does not actually store anything

The `--stdin` option tells git hash-object to use the content from stdin rather than a file. In our example, it will hash the word 'hello'

`echo 'hello' | git hash-object --stdin`

The echo command simply repeats whatever we tell it to repeat to the terminal. We pipe the output of echo to `git hash-object`.

Rather than simply outputting the key that git would store our object under, we can use the **-w** option to tell git to actually write the object to the database.

`echo 'hello' | git hash-object --stdin -w`

After running this command, check out the contents of **.git/objects**
