# Git Collaboration Work Flows

## Centralized Workflow

AKA Everyone Works On Master/Main

The simplest collaborative workflow is to have everyone work on the master branch (or main, or any other SINGLE branch).

It's straightforward and can work for tiny teams, but it has quite a few shortcomings!

### The Problem

While it's nice and easy to only work on the master branch, this leads to some serious issues on teams!

- Lots of time spent resolving conflicts and merging code, especially as team size scales up.

- No one can work on anything without disturbing the main codebase. How do you try adding something radically different in? How do you experiment?

- The only way to collaborate on a feature together with another teammate is to push incomplete code to master. Other teammates now have broken code...

## Feature Branches

Rather than working directly on master/main, all new development should be done on separate branches!

- Treat master/main branch as the official project history
- Multiple teammates can collaborate on a single feature and share code back and forth without polluting the master/main branch
- Master/main branch won't contain broken code (or at least, it won't unless someone messes up)

> In conclusion, feature branches is much better option than centralized workflow to work with collaborators.
