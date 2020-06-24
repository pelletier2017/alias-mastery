# Exit codes and Conditionals

Each command typed in a shell has an exit code. 0 means success and non-zero means failure. Note that $? only applies to the last ran command.
```bash
$ echo hello
hello

$ echo $?
0

$ cat doesntExist.txt
cat: doesntExist.txt: No such file or directory

$ echo $??
1
```

The && operator will only proceed to the next command if the previous command was successful.
```bash
$ echo "hello" && echo "still going"
hello
still going

$ cat doesntExist.txt && echo "will not print"
cat: doesntExist.txt: No such file or directory
```

The || operator will only proceed to the next command if the first failed
```bash
$ echo "hello" || echo "wont print"
hello

$ cat doesntExist.txt || echo "will print"
cat: doesntExist.txt: No such file or directory
will print

$ echo $?
0
```

The ; symbol represents a new-line so the commands will always run nomatter what
```bash
$ echo "hello"; echo "hello again"
hello
hello again

$ cat doesntExist.txt; echo "prints nomatter what"
cat: doesntExist.txt: No such file or directory
prints nomatter what
```

Exercise:
1. Write an alias `show_user` to `cat` the file `user.txt` if it exists or print "user.txt doesnt exist" if it doesn't
2. Write an alias `user` that uses both `find_user` and `show_user`. It should only run `show_user` if `find_user` was successful.
