# Alias basics

### Creating an alias

``` bash
$ alias myAlias="echo hello"
```

### Show newly created alias
``` bash
$ alias
alias myAlias="echo hello"
```

### Use alias
``` bash
$ myAlias
hello
```

Aliases only last until you close your terminal. So to make them persist, we have to add the alias to a file that will be loaded whenever a new terminal is opened. On linux and mac, these files are `~/.bash_profile` or `~/.bash_rc`.

`.bash_profile` is ran whenever logging into a new terminal

`.bash_rc` is ran whenever starting a new terminal with `bash` command

In general I put everything in `~/.bash_profile` and don't worry about it.

Load aliases without starting a new terminal
```bash
# source <file>
source ~/.bash_profile
```

Exercise:
1. Inside of your `~/.bash_profile` create an alias to list all files in your home directory an call it "ls_home"
2. source your `.bash_profile` to load the alias
3. use the command `alias` to confirm it was loaded and run it with `ls_home`
