

## Create user
Create user with new home directory etc.
```
adduser <username>
```
## Add user to group
```
usermod -aG <group e.g. sudo> <username>
```
## Delete user
```
deluser --remove-home <username>
```

## SCP
```
scp .\localfile bart@a.b.x.d:/home/bart
```