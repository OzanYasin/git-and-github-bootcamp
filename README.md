# Git Tags

Tags are pointers that refer to particular points in Git history. We can mark a particular moment in time with a tag. Tags are most often used to mark version releases in projects (v4.1.0, v4.1.1, etc.)

Think of tags as branch references that do NOT CHANGE. Once a tag is created, it always refers to the same commit. It's just a label for a commit.

## The Two Types

There are two types of Git tags we can use: lightweight and annotated tags

**lightweight tags are...lightweight.** They are just a name/label that points to a particular commit.

**annotated tags** store extra meta data including the author's name and email, the date, and a tagging message (like a commit message)

## Semantic Versioning

The semantic versioning spec outlines a standardized versioning system for software releases. It provides a consistent way for developers to give meaning to their software releases (how big of a change is this release??)

Versions consist of three numbers separated by periods.

**Documents: https://semver.org**

### **Initial Release**

Typically, the first release is 1.0.0

### **Patch Release**

Patch releases normally do not contain new features or significant changes. They typically signify bug fixes and other changes that do not impact how the code is used.

> 1.0.1

### **Minor Release**

Minor releases signify that new features or functionality have been added, but the project is still backwards compatible. No breaking changes. The new functionality is optional and should not force users to rewrite their own code.

> 1.1.0

### **Major Release**

Major releases signify significant changes that is no longer backwards compatible. Features may be removed or changed substantially.

> 2.0.0

## Viewing Tags

`git tag` will print a list of all the tags in the current repository.

We can search for tags that match a particular pattern by using git tag -l and then passing in a wildcard pattern. For example, `git tag -l "*beta*"` will print a list of tags that include "beta" in their name.

## Checking Out Tags

To view the state of a repo at a particular tag, we can use `git checkout <tag>`. _This puts us in detached HEAD!_

## Creating Lightweight Tags

To create a lightweight tag, use `git tag <tagname>`.

By default, Git will create the tag referring to the commit that HEAD is referencing.

## Creating Annotated Tags

Use `git tag -a <tagname>` to create a new annotated tag. Git will then open your default text editor and prompt you for additional information.

Similar to git commit, we can also use the -m option to pass a message directly and forgo the opening of the text editor
