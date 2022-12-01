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

## Feature Branch Naming

There are many different approaches for naming feature branches. Often you'll see branch names that include slashes like **bug/fix-scroll** or **feature/login-form** or **feat/button/enable-pointer-events**

Specific teams and projects usually have their own branch naming conventions. To keep these slides simple and concise, I'm just going to ignore those best-practices for now.

## Merging In Feature Branches

At some point new the work on feature branches will need to be merged in to the master branch!  
There are a couple of options for how to do this...

1.  Merge at will, without any sort of discussion with teammates. JUST DO IT WHENEVER YOU WANT.
2.  Send an email or chat message or something to your team to discuss if the changes should be merged in.
3.  Pull Requests!

## Pull Requests

Pull Requests are a feature built in to products like Github & Bitbucket. **They are not native to Git itself**.

They allow developers to alert team-members to new work that needs to be reviewed. They provide a mechanism to approve or reject the work on a given branch. They also help facilitate discussion and feedback on the specified commits.

_"I have this new stuff I want to merge in to the master branch...what do you all think about it?"_

> If there is conflicts, you should resolve that by following the instructors on Github.

## The Workflow

1.  Do some work locally on a feature branch
2.  Push up the feature branch to Github
3.  Open a pull request using the feature branch just pushed up to Github
4.  Wait for the PR to be approved and merged. Start a discussion on the PR. This part depends on the team structure.

## Fork & Clone: Another Workflow

The **"fork & clone"** workflow is different from anything we've seen so far. Instead of just one centralized Github repository, every developer has their own Github repository in addition to the "main" repo. Developers make changes and push to their own forks before making pull requests.

It's very commonly used on large open-source projects where there may be thousands of contributors with only a couple maintainers.

## Forking

Github (and similar tools) allow us to create personal copies of other peoples' repositories. We call those copies a "fork" of the original.

When we fork a repo, we're basically asking Github "Make me my own copy of this repo please"

As with pull requests, forking is not a Git feature. The ability to fork is implemented by Github.
