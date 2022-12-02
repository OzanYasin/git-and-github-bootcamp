# Git Tags

Tags are pointers that refer to particular points in Git history. We can mark a particular moment in time with a tag. Tags are most often used to mark version releases in projects (v4.1.0, v4.1.1, etc.)

Think of tags as branch references that do NOT CHANGE. Once a tag is created, it always refers to the same commit. It's just a label for a commit.

## The Two Types

There are two types of Git tags we can use: lightweight and annotated tags

lightweight tags are...lightweight. They are just a name/label that points to a particular commit.

annotated tags store extra meta data including the author's name and email, the date, and a tagging message (like a commit message)
