<!---
  Name          : Chapter_13.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 13 exercise problems

--->


# Chapter 13 Exercise Problems

### 1.
Run `traceroute` to your favorite website. How many hops appear between you and your favorite site?

---

````shell
┌──(root💀Kali)-[/]
└─# sudo apt-get install traceroute                                                                                                            
Reading package lists... Done
--snip--
┌──(root💀Kali)-[/]
└─# traceroute github.com                                                                                                                              1 ⚙
traceroute to github.com (140.82.121.3), 30 hops max, 60 byte packets
 1  10.0.2.2 (10.0.2.2)  0.386 ms  0.285 ms  0.224 ms

--snip--
````

---


### 3.
Try using `proxychains` with the Firefox browser to navigate to your favorite website.

---

````shell
┌──(root💀Kali)-[/]
└─#  proxychains firefox github.com                                                                                                                    1 ⚙
[proxychains] config file found: /etc/proxychains4.conf
[proxychains] preloading /usr/lib/x86_64-linux-gnu/libproxychains.so.4
[proxychains] DLL init: proxychains-ng 4.14
[proxychains] DLL init: proxychains-ng 4.14
[proxychains] DLL init: proxychains-ng 4.14
Running Firefox as root in a regular user's session is not supported.  ($XAUTHORITY is /home/ahmed/.Xauthority which is owned by ahmed.)

````

---



