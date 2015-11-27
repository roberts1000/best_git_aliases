# best-git-aliases
best-git-aliases is a curated collection of the useful aliases for git.  If you have a new alias to share, submit a Pull Request!

<br />

## Getting Started
First, read the [Working With Aliases](#working-with-aliases) section below to understand how to add, remove and list Git aliases.  Then, scroll down to [The List](#the-list) below and pick out your alises.  Each alias definition in the list includes

```
1. alias name
2. alias description
3. terminal command to add the alias
```

<br />

## Working With Aliases

### Listing Aliases
There are many ways to see the list of currently defined aliases.
```
git config --get-regexp '^alias\.'
git config --list
git config --l
git config --l | grep alias
```

### Adding Aliases
Aliases can be added by 1) executing a command in the terminal or 2) directly editing the `.gitconfig` file on your system.  

**By Command**

```
git config --global alias.<alias-name-here> '<git-command(s)-to-alias-here>'
```

**Direct File Edit**

The file is located in different places depending on your system:

1. **Linux:** ~/.gitconfig
2. **Windows 7:** C:\Users\\&lt;username-here&gt;\\.gitconfig

Once you have found the file, open it with the editor of your choice.  

### Deleting Aliases
Aliases can be deleted with:

`git config --global --unset alias.<alias-name-here>`

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
