1)
Checking swappiness on all my nodes with cat /proc/sys/vm/swappiness, output -> 60
changing it to 1 with sysctl vm.swappiness=1
2)
cat /proc/mount to show the mount points of all volumes

rootfs / rootfs rw 0 0
proc /proc proc rw,relatime 0 0
sysfs /sys sysfs rw,seclabel,relatime 0 0
devtmpfs /dev devtmpfs rw,seclabel,relatime,size=7637860k,nr_inodes=1909465,mode=755 0 0
devpts /dev/pts devpts rw,seclabel,relatime,gid=5,mode=620,ptmxmode=000 0 0
tmpfs /dev/shm tmpfs rw,seclabel,relatime 0 0
/dev/xvda1 / ext4 rw,seclabel,relatime,barrier=1,data=ordered 0 0
none /selinux selinuxfs rw,relatime 0 0
devtmpfs /dev devtmpfs rw,seclabel,relatime,size=7637860k,nr_inodes=1909465,mode=755 0 0
/proc/bus/usb /proc/bus/usb usbfs rw,relatime 0 0
none /proc/sys/fs/binfmt_misc binfmt_misc rw,relatime 0 0

3)lsblk --output NAME,FSTYPE,UUID,MODE

NAME    FSTYPE UUID                                 MODE
xvda                                                brw-rw----
+-xvda1 ext4   b48e599f-bd30-4876-9a63-ecd015ba7454 brw-rw----

4) vi /boot/grub/grub.conf
	added at the end of the file  transparent_hugepage=never
	
5)ip link show
	1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
	2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc pfifo_fast state UP qlen 1000
    link/ether 02:06:58:14:e7:18 brd ff:ff:ff:ff:ff:ff
	
6)getent hosts 35.157.161.230
	35.157.161.230  ec2-35-157-161-230.eu-central-1.compute.amazonaws.com

  getent ahosts google.com
	172.217.21.238  STREAM google.com
	172.217.21.238  DGRAM
	172.217.21.238  RAW
	2a00:1450:4001:80b::200e STREAM
	2a00:1450:4001:80b::200e DGRAM
	2a00:1450:4001:80b::200e RAW
7-8) these 2 services were not installed, therefor i installed them with yum install ntp, yum install nscd.
	 to start them -> service nscd start, service ntpd start
	 to show the status -> service nscd status, service ntpd status