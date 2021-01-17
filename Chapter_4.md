<!---
  Name          : Chapter_4.md
  Project       : Linux Basics for Hackers 1e
  Description   : Solutions to chapter 4 exercise problems
--->


# Chapter 4 Exercise Problems

### 1.
Install a new software package from the Kali repository.

---

````shell
┌──(root💀Kali)-[/]
└─# apt-get install git                                                                                                                              100 ⨯
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  git-man
Suggested packages:
  git-daemon-run | git-daemon-sysvinit git-doc git-el git-email git-gui gitk gitweb git-cvs git-mediawiki git-svn
The following packages will be upgraded:
  git git-man
2 upgraded, 0 newly installed, 0 to remove and 954 not upgraded.
Need to get 7,182 kB of archives.
After this operation, 11.5 MB disk space will be freed.
Do you want to continue? [Y/n] y
Get:1 http://kali.download/kali kali-rolling/main amd64 git amd64 1:2.29.2-1 [5,373 kB]
Get:2 http://kali.download/kali kali-rolling/main amd64 git-man all 1:2.29.2-1 [1,809 kB]
Fetched 7,182 kB in 6s (1,150 kB/s)                                                                                                                       
(Reading database ... 261763 files and directories currently installed.)
Preparing to unpack .../git_1%3a2.29.2-1_amd64.deb ...
Unpacking git (1:2.29.2-1) over (1:2.28.0-1) ...
Preparing to unpack .../git-man_1%3a2.29.2-1_all.deb ...
Unpacking git-man (1:2.29.2-1) over (1:2.28.0-1) ...
Setting up git-man (1:2.29.2-1) ...
Setting up git (1:2.29.2-1) ...
Processing triggers for man-db (2.9.3-2) ...
Processing triggers for kali-menu (2020.4.0) ...


````

---


### 2.
Remove that same software package.

---

````shell
┌──(root💀Kali)-[/]
└─#  apt-get remove git
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following packages were automatically installed and are no longer required:
  ettercap-common ettercap-graphical figlet finger git-man libapache2-mod-php liberror-perl libluajit-5.1-2 libluajit-5.1-common medusa
  oracle-instantclient-basic python3-aioredis python3-apscheduler python3-gitdb python3-pefile python3-pyfiglet python3-pyshodan python3-qrcode
  python3-quamash python3-smmap python3-tld python3-yaswfp rwho rwhod sparta-scripts toilet-fonts wapiti xsltproc
Use 'sudo apt autoremove' to remove them.
The following packages will be REMOVED:
  commix git kali-linux-default kali-linux-headless kali-tools-top10 legion metasploit-framework msfpc python3-git python3-pyexploitdb set unicorn-magic
0 upgraded, 0 newly installed, 12 to remove and 948 not upgraded.
After this operation, 508 MB disk space will be freed.
Do you want to continue? [Y/n] y
(Reading database ... 261758 files and directories currently installed.)
Removing kali-linux-default (2020.4.8) ...
Removing kali-linux-headless (2020.4.8) ...
Removing commix (3.1-0kali1) ...
Removing legion (0.3.7-0kali2) ...
Removing python3-pyexploitdb (0.2.0+20190604-0kali5) ...
Removing python3-git (3.1.9-1) ...
Removing msfpc (1.4.5-0kali1) ...
Removing kali-tools-top10 (2020.4.8) ...
Removing set (8.0.3+git20200609-0kali2) ...
Removing unicorn-magic (3.12-0kali1) ...
Removing metasploit-framework (6.0.15-0kali1) ...
Removing git (1:2.29.2-1) ...
Processing triggers for man-db (2.9.3-2) ...
Processing triggers for kali-menu (2020.4.0) ...

````

---


### 3.
Update your repository.

---

````shell
┌──(root💀Kali)-[/]
└─# apt-get update
Get:1 http://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]                         
Get:3 http://dl.google.com/linux/chrome/deb stable/main amd64 Packages [1,095 B]               
Get:2 http://kali.download/kali kali-rolling InRelease [30.5 kB]
Get:4 http://kali.download/kali kali-rolling/main amd64 Packages [17.5 MB]
Get:5 http://kali.download/kali kali-rolling/contrib amd64 Packages [106 kB]                                                                              
Get:6 http://kali.download/kali kali-rolling/non-free amd64 Packages [202 kB]                                                                             
Fetched 17.8 MB in 9s (2,077 kB/s)                                                                                                                        
Reading package lists... Done

````

---


### 4.
Upgrade your software packages.

---

````shell
┌──(root💀Kali)-[/]
└─#  sudo apt upgrade
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Calculating upgrade... Done
The following packages were automatically installed and are no longer required:
  ettercap-common ettercap-graphical figlet finger libapache2-mod-php libcapstone3 libcrypto++6 libexo-1-0 libexo-helpers libgdal27 libgeos-3.8.1
  libllvm10 libluajit-5.1-2 libluajit-5.1-common libmicrohttpd12 libplymouth4 libpython3.8 libpython3.8-dev libpython3.8-minimal libpython3.8-stdlib
  libqt5opengl5 libradare2-4.3.1 libwireshark13 libwiretap10 libwsutil11 libxcb-util0 medusa oracle-instantclient-basic python3-aioredis
  python3-apscheduler python3-gevent python3-gitdb python3-greenlet python3-pefile python3-pyfiglet python3-pyshodan python3-qrcode python3-quamash
  python3-smmap python3-tld python3-yaswfp python3-zope.event python3.8 python3.8-dev python3.8-minimal qt5-gtk2-platformtheme ruby-connection-pool
  ruby-molinillo ruby-net-http-persistent ruby-thor rwho rwhod sparta-scripts toilet-fonts wapiti xfce4-mailwatch-plugin xfce4-smartbookmark-plugin
  xfce4-statusnotifier-plugin xfce4-weather-plugin xsltproc
Use 'sudo apt autoremove' to remove them.
--snip--
````

---


### 5.
Select a new piece of software from github and clone it to your system.

---

````shell
┌──(root💀Kali)-[/]
└─# git clone https://github.com/digininja/DVWA.git
Cloning into 'DVWA'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3313 (delta 0), reused 0 (delta 0), pack-reused 3310
Receiving objects: 100% (3313/3313), 1.60 MiB | 95.00 KiB/s, done.
Resolving deltas: 100% (1473/1473), done.

````

---
