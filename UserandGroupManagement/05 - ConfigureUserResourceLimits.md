# Configure user resource limits
It limits the use of system-wide resources
```
ulimit
```

Limits can be configured changing file `/etc/security/limits.conf`

Typical configuration
```bash
1. @student        hard    nproc           20
2. @faculty        soft    nproc           20
3. ftp             hard    nproc           0
4. @student        -       maxlogins       4
```

1. Members of student group can run only 20 processes
2. Members of faculty group will receive and info after that more than 20 processes were run (soft limit)
3. ftp user cannot run any process
4. Members of student can have maximum 4 logged user. - means both hard and soft

`man limits.conf` for manual

Limits will be enforced in next opened session. Also `ulimit` command can be used to change limits