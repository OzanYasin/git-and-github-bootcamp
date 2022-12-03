# Git Reflogs: Retrieving Lost Work

Git keeps a record of when the tips of branches and other references were updated in the repo.

We can view and update these reference logs using the `git reflog` command.

> Git only keeps reflogs on your **local** activity. They are not shared with collaborators. Reflogs also expire. Git cleans out old entries after around 90 days, though this can be configured.
