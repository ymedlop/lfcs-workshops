# List, set, and change standard file permissions
To see user, group and permission use `ls -l`. Permissions are in the first column, name in third and group in fourth. Each file/directory will have an *owner* and will be associated to a *group*.

The permissions for each file/directory are given for each of this category:
* Owner
* Group
* Others

The right that each permission provide are different and depends if target is a file or a directory:

|           |     File     |   Directory   |
| :-------: | :----------: | :-----------: |
| Read (4)  | Read or Exec |   List (ls)   |
| Write (2) |    Modify    | Create Delete |
| Exec (1)  |     Run      |      cd       |

**Note**: When exec is set for group of other, file will be executed with identity of the user that are executing command (user ID) and group of user (group ID)

## Absolute mode:
Use numbers for each permission, that must be added if more that a permission 

`chmod 760 file` Change file permission
  * Owner: grant read, write and exec
  * Group: grant read, write
  * Others: no permission

## Relative mode:
```
chmod +x file - Add exec to owner, group and other
chmod g+w file - Add write to group
chmod o-rw file - Remove read and write to others
```

## Advanced permissions
There are other special permissions that can be granted to file/dirctories

|                |         File         |                          Directory                          |
| :------------: | :------------------: | :---------------------------------------------------------: |
|    suid (4)    | Run as owner of file |                             N/A                             |
|    sgid (2)    |  Run as group owner  |       Inherit directory group when a file is created        |
| sticky bit (1) |         N/A          | A file can be deleted only by owner or by directory's owner |

**Note**
* **suid** When a file with setuid is executed, the resulting process will assume the effective user ID given to the owner class. This enables users to be treated temporarily as root (or another user). E.g `passwd` has suid setted 
* **sgid**:  When a file with *setgid* is executed, the resulting process will assume the group ID given to the group class
* Sticky bit is applied to /tmp
* Suid cannot be applied to Bash scripts

### Absolute mode:
`chmod 4760 file` Change file permission
  - Add suid
  - Owner: grant read, write and exec
  - Group: grant read, write
  - Others: no permission

### Relative mode:
```
chmod u+s file - set suid
chmod g+s file - set guid
chmod +t dir - set sticky bit
```
