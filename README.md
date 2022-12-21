# 0x16. C - Simple Shell


# Requirements

Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.
The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (See below)
### Example of error with sh:
```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```
### Same error with your program hsh:
```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```
# List of allowed functions and system calls
- ```access``` (man 2 access) - ```exit``` (man 3 exit) - ```chdir``` (man 2 chdir)



- ```close``` (man 2 close) | ```closedir``` (man 3 closedir) | ```closedir``` (man 3 closedir)



- ```execve``` (man 2 execve)| ```_exit``` (man 2 _exit)| ```fflush``` (man 3 fflush)




- ```fork``` (man 2 fork) | ```free``` (man 3 free)| ```getline``` (man 3 getline)
- ```getcwd``` (man 3 getcwd)| ```getpid``` (man 2 getpid)| ```isatty``` (man 3 isatty)


- ```kill``` (man 2 kill)| ```malloc``` (man 3 malloc) | ```open``` (man 2 open)

- ```opendir``` (man 3 opendir)| ```perror``` (man 3 perror)| ```read``` (man 2 read)

- ```readdir``` (man 3 readdir)| ```signal``` (man 2 signal)| ```stat``` (__xstat) (man 2 stat)

- ```lstat``` (__lxstat) (man 2 lstat)| ```fstat``` (__fxstat) (man 2 fstat)| ```strtok``` (man 3 strtok)

- ```wait``` (man 2 wait)| ```waitpid``` (man 2 waitpid)| ```wait3``` (man 2 wait3)
- ```wait4``` (man 2 wait4) | ```write``` (man 2 write)



# How to compile
## The shell will be complied with this:

`gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`


# File Description

- `execute.c` - execute the command.
- `prompt.c` - it use getline system call to read the input from the user and run infinite loop with fork to keep prompt going.
- `special_character` - It identiies if the special inputs such as if the frist input is slash,the user typed exit or env...
- `man_1_simple_shell` - is the man page for the shell we are going to write.
- `AUTHORS` - file at the  root of your repository, listing all individuals having contributed content to the repository. 
- `main.h` - is the header file 
- `main.c` - initialize the program with infinite loop by call the prompt function
- `string.c` -it handles the strings(string length, write string,find string in directory,concatane strings....)
- `cmd.c` - it finds enterd command by the user.


  ```
