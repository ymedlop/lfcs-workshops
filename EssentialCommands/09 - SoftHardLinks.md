# Create and manage hard and soft links
```
ls -li - in first column show the i-node number
```

## Hard link
```
ln target newname - It will create and hard link to the same i-node of target with name (filename) newname
```

# Symbolic link
```
ln -s target newlink - It will create a symbolic link to target called newlink

ln -s /var . - It will create a symbolic link to var in current directory. The name of link will be var
```

**Note**: A file is considered deleted when they don't exist anymore hard link to same i-node. This means that `rm` remove link, hard or symbolic.



