# Pipe and Redirection

### The output of one command can be used as the input to another command by using the symbol | 
```bash
$ cat myCats.txt
The Meowtain
Cat Drogo
Rhaego the cat who meownts the world!

# sed syntax is 's/fromWord/toWord/g'
$ cat myFile.txt | sed 's/Cat/Khal/g'
The Meowtain
Khal Drogo
Rhaego the cat who meownts the world!

$ cat myCats.txt | sort
Cat Drogo
Rhaego the cat who meownts the world!
The Meowtain

$ cat myFile.txt | grep -i "drogo"
Cat Drogo

$ cat myFile.txt | grep -i "drogo" | tr "[a-z]" "[A-Z]"
CAT DROGO
```

### Output of a command can be saved to a file
Note that this will overwrite whatever was in the file

```bash
$ echo "elephant" > animals.txt
$ cat animals.txt
elephant
```
### The redirected output could also append to a file instead

```bash
$ cat animals.txt
elephant

$ echo "lion" >> animals.txt

$ cat animals.txt
elephant
lion
```

Exercise:
1. Make sure you have the original file "params.txt" from the first exercise. Remove the old file "user.txt"
2. Use `cat` and `grep` together to find the "user" keyword.
3. Remove the keyword "user" from the string so we are left with just the value by using `sed`. Ex: "user=john" -> "john" 
(HINT: a sed string to delete a word has the "to" word empty 's/word//g'
4. Now add to the previous command to redirect the output to a file "user.txt"
5. `cat` the result file to confirm it contains the name of the user.
