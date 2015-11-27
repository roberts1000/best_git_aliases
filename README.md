# best-git-aliases
best-git-aliases is a community-driven list of aliases for git.  If you have a new alias to share, submit a Pull Request!

<br />

## Getting Started

### Show Currently Defined Aliases
There are many ways to see the list of currently defined aliases.
```
git config --get-regexp alias
git config --list
```

### How to Add an Alias
Aliases can be added to Git by 1) executing a command in the terminal or 2) directly editing the `.gitconfig` file on your system.  

**By Command**

```
git config --global alias.<alias name here> '<git command and options>'
```

**Direct File Edit**

The file is located in different places depending on your system:

1. **Linux:** ~/.gitconfig
2. **Windows 7:** C:\Users\ _username_\

Once you have found the file, open it with the editor of your choice.  

<br /><br />

## List of Aliases

#### aliases
List all currently defined aliases

`git config --global alias.aliases 'config --get-regexp alias'`

#### logg
Display a simple log graphic log with branch names

`git config --global alias.logg 'log --oneline --graph --decorate'`

#### state
`git config --global alias.state '!git fetch origin && git remote show origin && :'`

#### sync

`git config --global alias.sync '!git fetch origin && git remote prune origin && :'`
