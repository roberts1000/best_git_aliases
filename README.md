# best-git-aliases

best_git_aliases is a curated list of useful aliases for Git.

## Getting Started

First, read the [Working With Aliases](../../Working-With-Aliases.md) section to understand how to add, remove and list Git aliases. Then, head to [The List](#the-list).

## The List

#### alias

List all currently defined Git aliases.

    $ git config --global alias.alias "! git config --get-regexp ^alias\. | sed -e s/^alias\.// -e s/\ /\ =\ /"
    $ git config --global alias.alias "config --get-regexp '^alias\.'

#### logg

Display a simple graphic log with branch names.

    $ git config --global alias.logg 'log --oneline --graph --decorate'

#### remaster

Rebase the current branch on top of master. This command updates the local copy of `master` first, then rebases the current branch on top of `master`. This saves developers form having to switch over to master, `git pull`, then switch back to the feature branch to finally perform the rebase.

    $ git config --global alias.remaster '!git fetch origin master:master && git rebase master'

#### state

Show useful information about the state of the local repo relative to origin.

    $ git config --global alias.state '!git fetch origin && git remote show origin && :'

#### sync

Remove unneeded remote branches from the local repo. All branches deleted branches on the remote server, will still show up in the local repo when using commands like `branch` or aliases like `logg`. `sync` removes the refs to deleted remote branches if they are no longer needed locally.

    $ git config --global alias.sync '!git fetch origin && git remote prune origin && :'
