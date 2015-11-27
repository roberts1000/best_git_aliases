# Working With Aliases

### Listing Aliases
There are many ways to see the list of currently defined aliases.
```
git config --get-regexp '^alias\.'
git config --list
git config --l
git config --l | grep alias
```

### Adding Aliases
Aliases can be added by 1) executing a command in the terminal or 2) directly editing the `.gitconfig` file on your system.  Before adding an alias, you will need to identify the name of your alias and the command you would like to alias along with any any options.  It is possible to chain commands.

##### Adding By Command

`git config --global alias.<alias-name-here> '<git-command(s)-to-alias-here>'` 

##### Adding Direct File Edit

The file is located in different places depending on your system

1. **Linux:** ~/.gitconfig
2. **Windows 7:** C:\Users\\&lt;username-here&gt;\\.gitconfig

Once you have found the file, open it with the editor of your choice and add your new alias under the `[alias]` section.  Wehn adding aliases this way, each alias should be entered on its own line using the following template

```
<alias-name-here> = <command(s) and option to alias>
```

An example is

```
logg = log --oneline --graph --decorate
```

### Deleting Aliases
Aliases can be deleted with:

`git config --global --unset alias.<alias-name-here>`
