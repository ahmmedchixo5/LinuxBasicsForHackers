<!---
  Name          : Chapter_14.md
  Project       : Linux Basics for Hackers 1e
  Description   : Solutions to chapter 14 exercise problems
  Creation Date : 09 September 2020
  Author        : amenasec
  Link          : https://github.com/amenasec
--->


# Chapter 14 Exercise Problems

### 1.
Check your network devices with `ifconfig`. Note any wireless extensions.

---

````shell
┌──(root💀Kali)-[/]
└─# ifconfig                                                                                                                                           1 ⚙
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 194.168.1.1  netmask 255.255.255.0  broadcast 194.168.1.255
        inet6 fe80::a00:27ff:fee7:3053  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:e7:30:53  txqueuelen 1000  (Ethernet)
        RX packets 24268  bytes 30105937 (28.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4505  bytes 278674 (272.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 18  bytes 834 (834.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 18  bytes 834 (834.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

````

---


### 2.
Run `iwconfig` and note any wireless network adapters.

---
````shell
┌──(root💀Kali)-[/]
└─# iwconfig
lo        no wireless extensions.

eth0      no wireless extensions.
````
---


### 3.
Check to see what Wi-Fi AP's are in range with `iwlist`.

---

````shell
┌──(root💀Kali)-[/]
└─#  iwlist wlan0 scan                                                                                                                                 1 ⚙
wlan0     Interface doesn't support scanning.

````

---


### 4.
Check to see what Wi-Fi AP's are in range with `nmcli`. Which do you find more useful and intuitive, `nmcli` or `iwlist`?

---

````shell
┌──(root💀Kali)-[/]
└─#  nmcli dev wifi                                                                                                                              255 ⨯ 1 ⚙

````

---


### 5.
Connect to your Wi-Fi AP using `nmcli`.

---

````shell
┌──(root💀Kali)-[/]
└─#  nmcli dev wifi connect ***** password *****                                                                                               1 ⚙
Error: No Wi-Fi device found.

````

---


### 6.
Bring up your Bluetooth adapter with `hciconfig` and scan for nearby discoverable Bluetooth devices with `hcitool`.

---

````shell
┌──(root💀Kali)-[/]
└─# hciconfig hci0 up                                                                                                                              1 ⨯ 1 ⚙
Can't get device info: No such device
                                       
┌──(root💀Kali)-[/]
└─# hcitool scan                                                                                                                                   1 ⨯ 1 ⚙
Device is not available: No such device

````

---

### 7.
Test whether those Bluetooth devices are within reachable distance with `l2ping`.

---



---
