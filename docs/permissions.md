# Fixing Permissions Problems

To avoid potential permissions problems between host machine and containers (e.g. can't access files generated by PHP) you can add a group on your host machine with ID 82, it's a standard GID/UID for www-data user in Alpine Linux. 

## Linux

Create a new group with ID 82 and add yourself to this group.

```bash
sudo groupadd -r -g 82 alpine-www-data
sudo usermod -a -G alpine-www-data $(id -un)
```

Another solution is to use ACL mechanism, available on most of Linux distributions. 

It's available by default on Ubuntu, with ext4 filesystem (starting from 14.04 version). 
If you need more information, how to enable it on your Linux distribution, please check https://help.ubuntu.com/community/FilePermissionsACLs document. 


```bash
sudo setfacl -dR -m u:$(whoami):rwX -m u:82:rwX -m u:100:rX path_to_shared_volume
sudo setfacl -R -m u:$(whoami):rwX -m u:82:rwX -m u:100:rX path_to_shared_volume
```
Code above will make sure that both your current user and php-fpm have full permissions to all files, and nginx worker has read-only access to all files in workspace. 

## macOS

On macOS group with 82 already exists (_clamav). 

```bash
sudo dseditgroup -o edit -a $(id -un) -t user _clamav
```

## Windows

TBD