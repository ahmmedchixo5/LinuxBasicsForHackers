<!---
  Name          : Chapter_10.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 10 exercise problems
--->


# Chapter 10 Exercise Problems

### 1.
Use the `mount` and `umount` commands to mount and unmount your flash drive.

---

````shell
┌──(root💀Kali)-[/]
└─# mount /dev/sdb1 /media
┌──(root💀Kali)-[/]
└─# mount umount /dev/sdb1
````

---


### 2.
Check the amount of disk space free on your primary hard drive.

---

````shell
┌──(root💀Kali)-[/]
└─# df                                                                                                                                               127 ⨯
Filesystem     1K-blocks     Used Available Use% Mounted on
udev             4444104        0   4444104   0% /dev
tmpfs             895552      956    894596   1% /run
/dev/sda1       50356760 11234616  36534396  24% /
tmpfs            4477748        0   4477748   0% /dev/shm
tmpfs               5120        0      5120   0% /run/lock
tmpfs               4096        0      4096   0% /sys/fs/cgroup
tmpfs             895548       52    895496   1% /run/user/1000

````

---


### 3.
Check for errors on your flash drive with `fsck`.

---

````shell
┌──(root💀Kali)-[/]
└─# fsck -p /dev/sdb1 
--snip--
````

---


### 4.
Use the `dd` command to copy the entire contents of one flash drive to another, including deleted files.

---

````shell
┌──(root💀Kali)-[/]
└─#dd if=/dev/sdb1 of=/dev/sdc1
--snip--
````

---


### 5.
Use the `lsblk` command to determine basic characteristics of your block devices.

---

````shell
┌──(root💀Kali)-[/]
└─# lsblk                                                                                                                                              8 ⨯
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   50G  0 disk 
├─sda1   8:1    0   49G  0 part /
├─sda2   8:2    0    1K  0 part 
└─sda5   8:5    0  975M  0 part [SWAP]
sr0     11:0    1 1024M  0 rom  
                                
````

---
