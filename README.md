# Writing Git Custom Aliases

## Global Git Config

Git looks for the global config file at either **~/.gitconfig** or **~/.config/git/config**. Any configuration variables that we change in the file will be applied across all Git repos.

We can also alter configuration variables from the command line if preferred.

## Adding Aliases

We can easily set up Git aliases to make our Git experience a bit simpler and faster.

For example, we could define an alias **"git ci"** instead of having to type "git commit"

Or, we could define a custom **git lg** command that prints out a custom formatted commit log.

> On the command line, `git config --global alias.<custom-alias-name>` will do the same as editing config file in **.git** folder.

**Some Useful Aliases:** https://github.com/GitAlias/gitalias
