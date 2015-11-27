# best-git-aliases
best-git-aliases is a curated list of useful aliases for Git.  If you have a new alias to share, submit a Pull Request!

<br />

## Getting Started
First, read the [Working With Aliases](working-with-aliases.md) section to understand how to add, remove and list Git aliases.  Then, scroll down to [The List](#the-list) pick out your aliases.  Each alias definition in the list includes

**alias name**<br />
alias description

`terminal command to add the alias`
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

`git config --global alias.state '!git fetch origin && git remote show origin && :'`

**sync**<br />

`git config --global alias.sync '!git fetch origin && git remote prune origin && :'`
