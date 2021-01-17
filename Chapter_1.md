<!---
  Name          : Chapter_1.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 1 exercise problems
 
--->


# Chapter 1 Exercise Problems

### 1.
Use the `ls` command from the root (`/`) directory to explore the directory structure of Linux. Move to each of the directories with the `cd` command and run `pwd` to verify where you are in the directory structure.

---

````shell
┌──(root💀Kali)-[/]
└─# ls -l
total 68
lrwxrwxrwx   1 root root     7 Sep  6 12:30 bin -> usr/bin
drwxr-xr-x   3 root root  4096 Sep  6 12:41 boot
drwxr-xr-x  18 root root  3420 Sep  6 13:12 dev
drwxr-xr-x 157 root root 12288 Sep  6 13:02 etc
drwxr-xr-x   3 root root  4096 Sep  6 12:40 home
lrwxrwxrwx   1 root root    33 Sep  6 12:30 initrd.img -> boot/initrd.img-5.7.0-kali1-amd64
lrwxrwxrwx   1 root root    33 Sep  6 12:30 initrd.img.old -> boot/initrd.img-5.7.0-kali1-amd64
lrwxrwxrwx   1 root root     7 Sep  6 12:30 lib -> usr/lib
lrwxrwxrwx   1 root root     9 Sep  6 12:30 lib32 -> usr/lib32
lrwxrwxrwx   1 root root     9 Sep  6 12:30 lib64 -> usr/lib64
lrwxrwxrwx   1 root root    10 Sep  6 12:30 libx32 -> usr/libx32
drwx------   2 root root 16384 Sep  6 12:30 lost+found
drwxr-xr-x   3 root root  4096 Sep  6 12:30 media
drwxr-xr-x   2 root root  4096 Sep  6 12:30 mnt
drwxr-xr-x   2 root root  4096 Sep  6 12:30 opt
dr-xr-xr-x 220 root root     0 Sep  6 12:43 proc
drwx------   3 root root  4096 Sep  6 12:43 root
drwxr-xr-x  34 root root   820 Sep  6 12:48 run
lrwxrwxrwx   1 root root     8 Sep  6 12:30 sbin -> usr/sbin
drwxr-xr-x   3 root root  4096 Sep  6 12:39 srv
dr-xr-xr-x  13 root root     0 Sep  6 12:43 sys
drwxrwxrwt  15 root root  4096 Sep  6 13:18 tmp
drwxr-xr-x  14 root root  4096 Sep  6 12:32 usr
drwxr-xr-x  12 root root  4096 Sep  6 12:32 var
lrwxrwxrwx   1 root root    30 Sep  6 12:30 vmlinuz -> boot/vmlinuz-5.7.0-kali1-amd64
lrwxrwxrwx   1 root root    30 Sep  6 12:30 vmlinuz.old -> boot/vmlinuz-5.7.0-kali1-amd64
````

---


### 2.
Use the `whoami` command to verify which user you are logged in as.

---

````shell
┌──(root💀Kali)-[/]
└─# whoami
root

````

---


### 3.
Use the `locate` command to find wordlists that can be used for password cracking.

---

````shell
┌──(root💀Kali)-[/]
└─# locate wordlists
/usr/bin/wordlists
/usr/lib/python3/dist-packages/theHarvester/wordlists
/usr/share/wordlists
/usr/share/amass/wordlists
/usr/share/amass/wordlists/all.txt
/usr/share/amass/wordlists/bitquark_subdomains_top100K.txt
/usr/share/amass/wordlists/deepmagic.com_top500prefixes.txt
--snip--
/var/lib/dpkg/info/wordlists.prerm
````

---


### 4.
Use the `cat` command to create a new file and then append to that file. Keep in mind that `>` redirects input to a file and `>>` appends to a file.

---

````shell
┌──(root💀Kali)-[/]
└─# cat > newfile
This is my new file.
┌──(root💀Kali)-[/]
└─# cat >> newfile
This is my appendage.
┌──(root💀Kali)-[/]
└─# cat newfile
This is my new file.
This is my appendage.
````

---


### 5.
Create a new directory called `hackerdirectory` and create a new file that directory named `hackedfile`. Now copy that file to your `/root` directory and rename it `secretfile`.

---

````shell

┌──(root💀Kali)-[/home/ahmed]
└─#  mkdir hackerdirectory
┌──(root💀Kali)-[/home/ahmed]
└─# touch hackerdirectory/hackedfile
┌──(root💀Kali)-[/home/ahmed]
└─# cp hackerdirectory/hackedfile /root/secretfile
````

---
