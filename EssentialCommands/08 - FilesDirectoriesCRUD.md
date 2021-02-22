# Create, delete, copy, and move files and directories

You must be able to check results of activities.

* `ls` list directory content

  * `ls -l` long output. It will print more columns 

    File Type+Permissions - Number of links - Owner - Group - Dimension - Creation date - Creation hour - Name

    First letter of first column indicate file type:

    * `-` : file
    * `d`: directory
    * `l`: link

  * `ls -la` long output plus hidden files

  * `ls -lR` long output recursive (show subdirectories content)

  * `ls -lt` long output sorted by modification time

  * `ls -ld /etc` show the directory properties and not its content



* `du file` show disk usage
  * `du directory` show space used by directory and each subdirectory. It is recursive
  * `du -s directory` summarize space used by directory and subdirectory
  * `du *` show space of each file in current directory
* `pwd` print current directory



- `touch file`

  It creates an empty file


* `cp source destination` copy source file to destination

  * `cp file1 file2 ./dest`

    Copy file2 and file2 to directory dest

  * `cp * ./dest`

    Copy all file of current directory to directory dest

  * `cp -r dir1 dir2`

    Copy dir1 in dir2. `-r` recursive

* `mkdir dir` create directory dir

  * `mkdir -p dir/dir2`

    Create a directory dir with a subdirecotory dir2

* `rmdir dir` remove dir. Note: dir must be empty
* `tree` show directories tree
  * `yum -y install tree` to install tree

* `mv file file2` rename file in file2
  * `mv file dir` move file in directory dir
  * `mv dir ..` move directory dir at the upper directory level
* `rm file` delete file
  * `rm -f file` remove read-only file
  * `rm -r dir` remove directory dir and all subdirectories and files