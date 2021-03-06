# Searching files

## [find](http://manpages.ubuntu.com/manpages/bionic/man1/find.1.html)
Search for files in a directory hierarchy
```
find /etc -name "\*host*" - Search in /etc all file/directories with host in their name. \* is a wildcard

find . -perm 777 -exec rm -f '{}' \;` -   Search from current position all files/directories with permissions 777 and after remove them

`-exec` uses the result of find to do something

`{}` will be substitute with result of find

The exec's command must be contained between `-exec` and `\;`. 

; is treated as end of command character in bash shell. For this I must escape it with \\. If escaped it will be interpreted by find and not by bash shell.

Some parameter accepts value n with + or - in front. The meaning is:
  * +n - for greater than n
  * -n - for less than n
  * n - for exactly n

find /etc -size -100k - Search in /etc all files/directories with size less of 100 kilobytes

find . -maxdepth 3 -type f -size +2M - Search starting from current position, descending maximum three directories levels, files with size major of 2 megabyte

find . \( -name name1 -o -name name2 \) - `-o` or, it is used to combine two conditions. \ is escape to avoid that ( or ) will be interpreted by bash shell

find . -samefile file - Find all files that have same i-node of file

find . \! -user owner - It will show all files that aren't owned by user owner. `!` means negation, but must be escaped by \ to  not be interpreted by bash shell

find . -iname name - Search name ignoring case

find . -perm 222 - Find all files with permissions equal to 222. E.g. only file with permissions 222 will be showed

find . -perm -222 - Find all files with at least permissions 222. E.g. 777 match as valid.

find . -perm /222 - Find all files with write for owner or write for group or write for others (at least one)

find . -perm -g=w - Find all files with at least  permission write for group

find . -atime +1 - Show all files accessed at least two days ago (more than 24 hours)
```

## [type](https://www.geeksforgeeks.org/type-command-in-linux-with-examples/)
The type command is used to describe how its argument would be translated if used as commands. It is also used to find out whether it is built-in or external binary file.
```
type locate
```

## [whereis](https://www.geeksforgeeks.org/whereis-command-in-linux-with-examples/)
whereis command is used to find the location of source/binary file of a command and manuals sections for a specified file in Linux system. 
```
type whereis
```

## [which](https://www.geeksforgeeks.org/which-command-in-linux-with-examples/)
which command in Linux is a command which is used to locate the executable file associated with the given command by searching it in the path environment variable. It has 3 return status as follows:
* 0 : If all specified commands are found and executable.
* 1 : If one or more specified commands is nonexistent or not executable.
* 2 : If an invalid option is specified.
```
type which
```