# Useful Linux Commands

### general commands

| command  | description                                                      |
|----------|------------------------------------------------------------------|
| man      | show description for a command                                   |
| echo     | print a string                                                   |
| history  | show all previous commands                                       |
| xargs    | convert multi-line input into command line args                  |
| clear    | clear terminal                                                   |
| vi       | open up text editor                                              |

### working with files
| command  | description                                                      |
|----------|------------------------------------------------------------------|
| ls       | list files in a directory                                        |
| cd       | change directory                                                 |
| pwd      | display present working directory                                |
| rm       | remove file or directory                                         |
| touch    | create file or update time stamps if it exists                   |
| cat      | print contents of file                                           |
| grep     | search input for a string                                        |
| mv       | move or rename file                                              |
| cp       | copy file                                                        |
| find     | find file by traversing the file system (up-to-date)             |
| locate   | find file by using pre-built database (faster)                   |
| diff     | find differences between two files                               |
| head     | display first few lines of a file                                |
| tail     | display last few lines of a file (or follow a file in real time) |
| mkdir    | create directory                                                 |

### working with users and permissions

| command  | description                                                      |
|----------|------------------------------------------------------------------|
| sudo     | run command as root user                                         |
| chmod    | change permissions for a file                                    |
| chown    | change owner for a file                                          |
| whoami   | displays current user                                            |
| groups   | displays current groups                                          |

### networking

| command  | description                                                      |
|----------|------------------------------------------------------------------|
| ssh      | create a terminal session on a remote machine                    |
| ping     | test connection to a hostname                                    |
| curl     | send a TCP or HTTP message                                       |
| wget     | just like curl but supports many more protocols                  |
| hostname | display hostname                                                 |

### resources
| command  | description                                                      |
|----------|------------------------------------------------------------------|
| df       | display free disk space                                          |
| du       | display disk usage                                               |
| top      | display processes with memory      

## Exercise
This is a simple chain of commands that we will build upon.
1. Copy the contents of the file `params.txt` into a file onto your computer. It is a file containing a list of key/value pairs.
2. Use grep (listed above) to find the key "user". Hint: `grep "pattern" filename`
3. Create a file `user.txt` that just contains the value of the user. For example if the line found in `params.txt` was "user=john" then put "john" into the file "user.txt".
