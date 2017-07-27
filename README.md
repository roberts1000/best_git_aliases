# best-git-aliases
best-git-aliases is a curated list of useful aliases for Git.  If you have a new alias to share, submit a Pull Request!

<br />

## Getting Started
First, read the [Working With Aliases](working-with-aliases.md) section to understand how to add, remove and list Git aliases.  Then, scroll down to [The List](#the-list) pick out your aliases.  Each alias definition in the list includes

**alias name**<br />
alias description

`terminal command to add the alias`<br />
`optional variations of the terminal command`

<br />

## The List

**alias**<br />
List all currently defined Git aliases.

`git config --global alias.alias "! git config --get-regexp ^alias\. | sed -e s/^alias\.// -e s/\ /\ =\ /"`<br />
`git config --global alias.alias "config --get-regexp '^alias\.'"`

**logg**<br />
Display a simple graphic log with branch names

`git config --global alias.logg 'log --oneline --graph --decorate'`

**state**<br />
Show useful information about the state of the local repo relative to origin.

`git config --global alias.state '!git fetch origin && git remote show origin && :'`

**sync**<br />
Remove dead remote branches from the local repo.  All branches deleted branches on the remote server, will still show up in the local repo when using commands like `branch` or aliases like `logg`.  `sync` removes the refs to deleted remote branches if they are no longer needed locally.

`git config --global alias.sync '!git fetch origin && git remote prune origin && :'`

**reebase-master**<br />
Rebase the current branch on top of master.  This command updates the local copy of `master` first, then rebases the current branch on top of `master`.  This saves developers form having to switch over to master, `git pull`, then switch back to the feature branch to finally perform the rebase.  The extra **e** in `reebase-master` is intentionally; it makes it easier to tab and use auto-completion after typing the second "e".

`git config --global alias.reebase-master = !git fetch origin master:master && git rebase master`

