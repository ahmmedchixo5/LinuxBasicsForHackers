<!---
  Name          : Chapter_9.md
  Project       : Linux Basics for Hackers 1e
  Description   : Solutions to chapter 9 exercise problems
--->


# Chapter 9 Exercise Problems

### 1.
Create three scripts to combine, similar to what we did in Chapter 8. Name them `Linux4Hackers1`, `Linux4Hackers2`, and `Linux4Hackers3`.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  echo $'#! /bin/bash\n\n echo "This is 1"' > Linux4Hackers1
┌──(ahmed㉿Kali)-[/home]
└─$  echo $'#! /bin/bash\n\n echo "This is 22"' > Linux4Hackers2
┌──(ahmed㉿Kali)-[/home]
└─$  echo $'#! /bin/bash\n\n echo "This is 333"' > Linux4Hackers3
````

---


### 2.
Create a tarball from these three files. Name the tarball `L4H`. Note how the size of the sum of the three files changes when they are tarred together.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  tar -cf L4H Linux4Hackers1 Linux4Hackers2 Linux4Hackers3
┌──(ahmed㉿Kali)-[/home]
└─$  ls -l Linux4Hackers? L4H
-rw-r--r-- 1 kali kali 10240 Sep  7 23:19 L4H
-rw-r--r-- 1 kali kali    32 Sep  7 23:16 Linux4Hackers1
-rw-r--r-- 1 kali kali    33 Sep  7 23:16 Linux4Hackers2
-rw-r--r-- 1 kali kali    34 Sep  7 23:16 Linux4Hackers3
````

---


### 3.
Compress the `L4H` tarball with `gzip`. Note how the size of the file changes. Investigate how you can control overwriting existing files. Now uncompress the `L4H` file.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  gzip L4H
┌──(ahmed㉿Kali)-[/home]
└─$  ls -l L4H.gz
-rw-r--r-- 1 kali kali 212 Sep  7 23:19 L4H.gz
┌──(ahmed㉿Kali)-[/home]
└─$  gunzip L4H.gz
````

---


### 4.
Repeat Exercise `3` with both `bzip2` and `compress`.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  bzip2 L4H
┌──(ahmed㉿Kali)-[/home]
└─$  ls -l L4H.bz2
-rw-r--r-- 1 kali kali 224 Sep  7 23:19 L4H.bz2
┌──(ahmed㉿Kali)-[/home]
└─$ bunzip2 L4H.bz2
````

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  compress L4H
┌──(ahmed㉿Kali)-[/home]
└─$  ls -l L4H.Z
-rw-r--r-- 1 kali kali 416 Sep  7 23:19 L4H.Z
┌──(ahmed㉿Kali)-[/home]
└─$  uncompress L4H.Z
````

---


### 5.
Make a physical, bit-by-bit copy of one of your flash drives using the `dd` command.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$ dd if=/dev/sdb of=/home/kali/flashcopy
--snip--
````

---
