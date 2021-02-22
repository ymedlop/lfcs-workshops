# Archive, backup, compress, unpack, and uncompress files

## tar
Save many files into a single file. File permissions are maintained by default only for file users. For other user I must explicit say to maintain permission during decompression using `-p` parameter
```
tar jcfv file.tar.bz2 * -Save all files of current directory in new bzip2 compressed file called file.tar.bz2

tar jxfv file.tar.bz2 - Extract content of file.tar.bz2

tar tf file.tar - Show content of file.tar. **Note**: the file.tar isn't compressed

tar --delete -f test.tar file - Delete file from test.tar. **Note**: the test.tar isn't compressed

tar --update -f test.tar file - Update file in test.tar. **Note**: the test.tar isn't compressed

tar X<(command that generate list) -c -f file.tar *

tar X<(ls | file -f - | grep -i MPEG | cut -d: -f 1) -c -f file.tar * - Exclude file MPEG from content of file.tar
```