## Add legacy key exchange protocols to SSH config on ansible host to be able to connect
Add the following lines to ```/etc/ssh/ssh_config```

```
KexAlgorithms +diffie-hellman-group14-sha1
PubkeyAcceptedAlgorithms +ssh-rsa #optional
HostkeyAlgorithms +ssh-rsa
```
## Add the following lines to known hosts file
``` 
+diffie-hellman-group14-sha1
```
