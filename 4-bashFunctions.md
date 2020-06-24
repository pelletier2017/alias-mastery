# Bash Functions

### Functions in bash can be used to make smarter aliases that can take arguments
```bash
$ function my_print() {
    echo "-----"
    echo $1
    echo "-----"
}

$ my_print "it prints!"
-----
it prints!
-----

# ssh into a docker container
# takes 1 argument, the name of the container
$ function docker_ssh() {
    docker exec -it "$1" /bin/sh
}

# ssh into the logstash container
$ docker_ssh logstash
```

### If not using a return statement, the exit code will be the last line of the function even if there are errors in the function
```bash
$ function has_error() {
    cat fileDoesntExist.txt
    echo "still going"
}

$ has_error
cat: fileDoesntExist.txt: No such file or directory
still going

$ echo $?
0

# returns 0 or 1 depending on the result of "cat mightFail.txt"
$ function smart_return() {
    cat mightFail.txt
    exit_code=$?
    
    echo "cleaning up"
    return $exit_code
}
```

To quit early you can chain commands together with &&
```bash
function describe_file() {
    file=$1
    echo $file && \
    cat $file && \
    echo "done describing file"
}

$ describe_file myCats.txt
myCats.txt
The Meowtain
Cat Drogo
Rhaego the cat who meownts the world!
done describing file

$ describe_file doesntExist.txt
doesntExist.txt
cat: doesntExist.txt: No such file or directory
```

Exercise

1. Create a function "ssh_into" to ssh into a machine with your username. It should take 1 argument which is the hostname of the machine to SSH into. (HINT: ssh -l <user> <hostname>)
2. Create an alias to ssh into a machine you commonly ssh into. Utilize your "ssh_into" function
