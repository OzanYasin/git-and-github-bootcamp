# Basics of Git

All Git Commands: https://git-scm.com/docs

## **Repository**

A Git "Repo" is a workspace which tracks and manages files within a folder.

Anytime we want to use Git with a project, app, etc we need to create a new git repository. We can have as many repos on our machine as needed, all with separate histories and contents

## **Initializing Git**

Use `git init` to create a new git repository. Before we can do anything git-related, we must initialize a repo first!

This is something you do once per project. Initialize the repo in the top-level folder containing your project≥

> DO NOT INIT A REPO INSIDE OF A REPO! Before running git init, use git status to verify that you are not currently inside of a repo.

## **Status Overview**

`git status` gives information on the current status of a git repository and its contents

It's very useful, but at the moment we don't actually have any repos to check the status of!

## **Commiting**

Making a commit is similar to making a save in a video game. We're taking a snapshot of a git repository in time.

When saving a file, we are saving the state of a single file. With Git, we can save the state of multiple files and folders together.

## **Adding**

We use the `git add` command to stage changes to be committed.

It's a way of telling Git, "please include this change in our next commit".≥

> Use `git add .` to stage all changes at once.

## **Git Commit**

We use the `git commit` command to actually commit changes from the staging area.

When making a commit, we need to provide a commit message that summarizes the changes and work snapshotted in the commit.

Running git commit will commit all staged changes. It also opens up a text editor and prompts you for a commit message.

This can be overwhelming when you're starting out...

So instead you can use the **-m flag** allows us to pass in an inline commit message, rather than launching a text editor.
