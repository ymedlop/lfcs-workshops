# Create, delete, and modify local groups and group memberships

## groupadd
Add group. When a group is created `/etc/group` file will be changed
Syntax:
* group_name: It is the name of group. If you run ls -l command, you will see this name printed in the group field.
* Password: Generally password is not used, hence it is empty/blank. It can store encrypted password. This is useful to implement privileged groups.
* Group ID (GID): group id
  * For each user must be assigned a group ID. You can see this number in your /etc/passwd file.
* Group List: It is a list of user names of users who are members of the group. The user names, must be separated by commas.
  * **NOTE**: The groups without group list are used as primary group for some users

## groupdel
Delete group

## groupmod
Modify group

## usermod
Add group to user
  * -G list of secondary groups
  * `-a` append. <u>**NOTE**: If not specified new group list will override current 
```
usermod -aG group user`
```