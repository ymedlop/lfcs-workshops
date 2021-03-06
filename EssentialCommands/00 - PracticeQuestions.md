# [LFCS Practice Questions](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)

## Question 1
Open the file under **/home/student/textreferences/editme.txt** and complete the following tasks:
1. Move line **7777** to line **1**.
2. Remove line **7000**.
3. Replace every occurrence of the word **Earth** shown with
an uppercase E, with the word **Globe**.
4. Add a new line at the very end of the document that
contains **Auctores Varii**

### Solution
1. ``
2. `sed -i '7000d' /home/student/textreferences/editme.txt`
3. `sed -i 's/Earth/Globe/g' /home/student/textreferences/editme.txt`
4. `echo 'Auctores Varii' >> /home/student/textreferences/editme.txt`

## Question 2
Working with archives and compressed files is an integral part of
the System Administrator’s job.
Perform the following tasks to demonstrate your ability to work
with archives and compressed files:
1. Extract all files from archive file /opt/SAMPLE001.zip
into target directory /opt/SAMPLE001
2. Create a tar archive file /opt/SAMPLE0001.tar
containing all files in the directory /opt/SAMPLE001
3. Compress the tar archive file /opt/SAMPLE0001.tar
using the bzip2 compression algorithm
4. Compress the tar archive file /opt/SAMPLE0001.tar
using the xz compression algorithm
Make sure that the uncompressed archive file
/opt/SAMPLE0001.tar is not removed after creating the
compressed versions of the archive file!

### Solution
TODO:

## Question 3
A data directory is not used anymore and is about to be archived.
You have been asked to identify and remove some files,before
archiving takes place.
Perform the following tasks to demonstrate your ability to search
for files given various criteria:
1. Find all executable files in the directory
/srv/SAMPLE002 and remove them
2. Find all files in the directory /srv/SAMPLE002, which
have not been accessed during the last month and
remove them
3. Find all empty directories in the directory
/srv/SAMPLE002 and remove them
4. Find all files in the directory /srv/SAMPLE002 with a file
extension of .tar. Write a list of matching filenames, one
per line, to the file
/opt/SAMPLE002/toBeCompressed.txt, which has
already been created. Ensure that you specify a relative
path to each file, using /srv/S

### Solution
1. `find /srv/SAMPLE002 -executable -type f -exec rm {} \;`
