# Compare and manipulate file content

## [diff](https://www.geeksforgeeks.org/diff-command-linux-examples/)
diff stands for difference. This command is used to display the differences in the files by comparing the files line by line.

Example: Compare file1 and file 2
```
diff file1 file2
```

Example: Compare file1 and file 2 with output in two columns
```
diff -y file1 file2
```

The important thing to remember is that diff uses certain special symbols and instructions that are required to make two files identical. It tells you the instructions on how to change the first file to make it match the second file.

### Special symbols are:
* a : add
* c : change
* d : delete

```
diff file1 file2
```

## [comm]()

## [cmp]()

## Editor: vi
The default editor that comes with the UNIX operating system is called vi (visual editor). The UNIX vi editor is a full screen editor and has two modes of operation:
* Command mode commands which cause action to be taken on the file, and
* Insert mode in which entered text is inserted into the file.

To use vi on a file, type in vi filename. If the file named filename exists, then the first page (or screen) of the file will be displayed; if the file does not exist, then an empty file and screen are created into which you may enter text.
```
vi file
```

### In command mode:
**Esc** - switch between *insert* to *command mode*
```
o - open a new line and enter in insert mode
O - open a new line above current position and enter in insert mode

:wq - write and quit
:q! - quit without save
:w! - force write

u - undo
ctrl + r - redo
gg - go to file begin
G - go to last line
dd - delete current line
x - delete current character
d$ - delete from current point to end of line

# Search
:/texttosearch
n - next occurence
N - previous occurence
:300 - go to line 300


# Replace:
:%s/one/ONE/g - replace all occurrences of one with ONE
:%s/one/ONE - replace first occurrences of one with INE

# Cut and paste:
v - select text
y - copy text selected text
p - paste copied text
d - delete selected text
```

### In insert mode:
**i** - switch between *command mode* to *insert mode*
```
uniq file - Remove equal consecutive rows
uniq -w 2 file - Remove equal consecutive rows comparing only first two characters
uniq -c file - Remove equal consecutive rows and show number of occurrences
sort file - order file content
sort -k 2 file - Order file content using as reference second word 
```

## [uniq](https://www.geeksforgeeks.org/uniq-command-in-linux-with-examples/)
Filter adjacent matching lines from INPUT (or standard input), writing to OUTPUT (or standard output). With no options, matching lines are merged to the first occurrence.
```
uniq file - Remove equal consecutive rows
uniq -w 2 file - Remove equal consecutive rows comparing only first two characters
uniq -c file - Remove equal consecutive rows and show number of occurrences
```

## [more]()

## [less]()

## [sort](https://www.geeksforgeeks.org/sort-command-linuxunix-examples/)
Order file content
```
sort file - Order file content
sort -k 2 file - Order file content using as reference second word 
```

## [cut](https://www.geeksforgeeks.org/cut-command-linux-examples/)
cut is a command-line utility that allows you to cut parts of lines from specified files or piped data and print the result to standard output. It can be used to cut parts of a line by delimiter, byte position, and character.
```
cut -d delimiter -f column
cut -d ' ' -f 1 file - Print first word of each line. Delimiter will be space
cut -d ' ' -f 1,3 file - Print first and third word of each line. Delimiter will be space
```

## [tail](https://www.geeksforgeeks.org/tail-command-linux-examples/)
The tail command is a command-line utility for outputting the last part of files given to it via standard input. It writes results to standard output. By default tail returns the last ten lines of each file that it is given. 
```
tail file - Print last 10 file lines
tail -n 5 - file Print last 5 file lines
tail -f file - Print last 10 file lines and append. Useful to monitor log files
```

## [head](https://www.geeksforgeeks.org/head-command-linux-examples/)
The head command is a command-line utility for outputting the first part of files given to it via standard input. It writes results to standard output. By default head returns the first ten lines of each file that it is given.
```
head file - Print first 10 file lines
head -n 2 file - Print first 2 file lines
```

## [tr](https://www.geeksforgeeks.org/tr-command-in-unix-linux-with-examples/)
The tr command in UNIX is a command line utility for translating or deleting characters. It supports a range of transformations including uppercase to lowercase, squeezing repeating characters, deleting specific characters and basic find and replace
```
tr SET1 SET2 - translate set of characters one to set of characters 2
cat file | tr test sub - It will replace all occurrences of test with sub
cat file | tr -s ' ' - It will replace all consecutive occurrences of space with one space
```

## [file](https://www.geeksforgeeks.org/file-command-in-linux-with-examples/)
```
file namefile - print the type of namefile
```

## [touch]()
