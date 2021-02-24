# Manage user privileges

**root** is the system administrator. When logged as root, shell prompts `#` character. Otherwise `$`

## su
```
su - Used to become root. It will continue to use the current session with user and group id substituted

su - Used to become root. It is same as logging into a fresh session on a terminal

su - user - Login as user.
```

## sudo
Command to allow an ordinary user to execute commands as a different user. In default configuration, group `wheel` is authorized to act as root. If a user is member of `wheel` can execute all command as root with this syntax:

To add user to wheel execute:
```
usermod -aG wheel username
```

Login as a root
```
sudo -i
```

## visudo
Modify the sudo configuration

Basic configuration:
```
demo ALL=(ALL:ALL)      ALL
    ​           The first field indicates the username that the rule will apply to.

demo ***ALL***=(ALL:ALL)      ALL
    ​           The first "ALL" indicates that this rule applies to all hosts.
demo ALL=(***ALL***:ALL)      ALL
    ​           This "ALL" indicates that user demo can run commands as all users.
demo ALL=(ALL:***ALL***)      ALL
    ​           This "ALL" indicates that user demo can run commands as all groups.
demo ALL=(ALL:ALL)      ***ALL***
    ​           The last "ALL" indicates these rules apply to all commands.
```

Whith this row inserted in sudo configuration, demo user can execute this command:
```
sudo -u user command
```

This means that it will execute command with the identity of user. If `-u` is not specified, this means that command will be executed as root.

demo user can open a root session running:
```
sudo su -
```