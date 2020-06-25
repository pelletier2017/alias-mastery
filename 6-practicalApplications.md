# Practical Application of aliases

### Why are aliases important
- reproducability
    - which command did I run last time?
- less congative load
    - focus on the difficult tasks, automate all the easy tasks
- no waiting around
    - don't wait for your first command to finish before typing the second
- I made this :)
    - feels good to write and test your own aliases
- encourages faster feedback
    - figure out fast rebuild once and use it over and over

### Practical Applications of aliases and functions
- common commands that are complex
- chain commands together that are always ran together
- rebuilding anything with 1 command
    - rebuild specific maven module (ex puppet modules)
    - rebuild docker image
    - cleanup docker, rebuild maven modules, and start application
    - hot deploy module into karaf

Exercise:
1. Write an alias to remove your existing app and clean up. It should return 0 even if there was nothing to clean up.
2. Write an alias to build your project (bonus if you can write 1 that runs tests and another that skips tests)
3. Write an alias to start your app
4. If you have tests that run after your app starts, write an alias to run those.
5. Chain all of the previous commands together into 1 alias to rebuild everything
