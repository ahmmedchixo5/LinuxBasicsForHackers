<!---
  Name          : Chapter_5.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 5 exercise problems
--->


# Chapter 5 Exercise Problems

### 1.
Select a directory and run a long listing on it. Note the permissions on the files and directory.

---

````shell
┌──(root💀Kali)-[/]
└─# ls -l                                                                                                                                              2 ⨯
total 92
lrwxrwxrwx   1 root root     7 Jan 12 10:12 bin -> usr/bin
drwxr-xr-x   3 root root  4096 Jan 12 10:29 boot
drwxr-xr-x  17 root root  3200 Jan 17 12:53 dev
drwxr-xr-x   2 root root  4096 Jan 16 16:51 directory
drwxr-xr-x  11 root root  4096 Jan 17 13:39 DVWA
drwxr-xr-x 155 root root 12288 Jan 17 13:22 etc
-rw-r--r--   1 root root    44 Jan 16 16:46 hackedfile
drwxr-xr-x   2 root root  4096 Jan 17 12:11 hackerdirectory

````

---


### 2.
Select a file you don't have permission to execute and give yourself execute permissions using the `chmod` command. Try using both the numerical method (`777`) and the UGO method.

---

````shell
┌──(root💀Kali)-[/usr/share/hashcat]
└─# ls -l 
-rw-r--r-- 1 root root  23281 Jul 31 09:09 hashcat.hctune

┌──(root💀Kali)-[/usr/share/hashcat]
└─# chmod 777 hashcat.hctune 

┌──(root💀Kali)-[/usr/share/hashcat]
└─# ls -l
-rwxrwxrwx 1 root root  23281 Jul 31 09:09 hashcat.hctune


┌──(root💀Kali)-[/usr/share/hashcat]
└─# chmod g-w,o-wx hashcat.hcstat
````

---


### 3.
Choose another file and change its ownership using `chown`.

---

````shell
┌──(ahmed㉿Kali)-[~]
└─$ ls -l
drwxr-xr-x 2 ahmed ahmed     4096 Jan 17 13:56 new

┌──(ahmed㉿Kali)-[~]
└─$ sudo  chown root ./new 

┌──(ahmed㉿Kali)-[~]
└─$ ls -l
drwxr-xr-x 2 root  ahmed     4096 Jan 17 13:56 new

````

---


### 4.
Use the `find` command to find all files with the `SGID` bit set.

---

````shell
┌──(root💀Kali)-[/]
└─# find / -perm -2000
find: ‘/proc/3361/task/3361/fd/5’: No such file or directory
find: ‘/proc/3361/task/3361/fdinfo/5’: No such file or directory
find: ‘/proc/3361/fd/6’: No such file or directory
find: ‘/proc/3361/fdinfo/6’: No such file or directory
find: ‘/run/user/1000/gvfs’: Permission denied
/run/postgresql
/run/log/journal
/usr/bin/chage
/usr/bin/write.ul
/usr/bin/ssh-agent
/usr/bin/wall
--snip--
````

---
