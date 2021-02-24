# Configure PAM
PAM = plugable authentication modules. A command/program can be PAM aware

Use ldd to see if command use PAM libraries
```
ldd /usr/bin/passwd | grep pam
```

Each command that will use PAM will have an entry in `/etc/pam.d` with its PAM configuration

A good example of PAM configuration is showed in pam_tally2 module man page
  * pam_tally2: The login counter (tallying) module

At the end of man page there is an example to configure login to lock the account after 4 failed logins
```
man pam_tally2
```
