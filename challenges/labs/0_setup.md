Cloude used -> AWS

Linux release -> centOS 7.4

[root@ip-172-31-44-19 /]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1       60G  824M   60G   2% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.3G     0  7.3G   0% /dev/shm
tmpfs           7.3G   17M  7.3G   1% /run
tmpfs           7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/1000



[root@ip-172-31-44-19 /]# yum repolist enabled
Loaded plugins: fastestmirror
base                                                                                                               | 3.6 kB  00:00:00
extras                                                                                                             | 3.4 kB  00:00:00
updates                                                                                                            | 3.4 kB  00:00:00
(1/4): base/7/x86_64/group_gz                                                                                      | 156 kB  00:00:00
(2/4): extras/7/x86_64/primary_db                                                                                  | 110 kB  00:00:00
(3/4): updates/7/x86_64/primary_db                                                                                 | 2.7 MB  00:00:00
(4/4): base/7/x86_64/primary_db                                                                                    | 5.7 MB  00:00:00
Determining fastest mirrors
 * base: mirror.23media.de
 * extras: mirror.imt-systems.com
 * updates: ftp.antilo.de
repo id                                                          repo name                                                          status
base/7/x86_64                                                    CentOS-7 - Base                                                    9,591
extras/7/x86_64                                                  CentOS-7 - Extras                                                    227
updates/7/x86_64                                                 CentOS-7 - Updates                                                   741
repolist: 10,559



[root@ip-172-31-44-19 /]# cat /etc/passwd | grep ernest
ernest:x:2000:3001::/home/ernest:/bin/bash
[root@ip-172-31-44-19 /]# cat /etc/passwd | grep siwicki
siwicki:x:3000:3002::/home/siwicki:/bin/bash



[root@ip-172-31-44-19 /]# cat /etc/group | grep usa
usa:x:3001:
[root@ip-172-31-44-19 /]# cat /etc/group | grep emea
emea:x:3002: