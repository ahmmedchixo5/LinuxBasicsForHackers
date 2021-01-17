<!---
  Name          : Chapter_15.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 15 exercise problems
--->


# Chapter 15 Exercise Problems

### 1.
Check the version of your kernel.

---

````shell
┌──(root💀Kali)-[/]
└─#  uname -a                                                                                                                                      1 ⨯ 1 ⚙
Linux Kali 5.9.0-kali1-amd64 #1 SMP Debian 5.9.1-1kali2 (2020-10-29) x86_64 GNU/Linux

````

---


### 2.
List the modules in your kernel.

---

````shell
┌──(root💀Kali)-[/]
└─# lsmod                                                                                                                                              1 ⚙
Module                  Size  Used by
bluetooth             729088  0
jitterentropy_rng      16384  1
drbg                   28672  1
ansi_cprng             16384  0
ecdh_generic           16384  1 bluetooth
ecc                    36864  1 ecdh_generic
fuse                  143360  3
rfkill                 28672  3 bluetooth
vboxsf                 40960  0
snd_intel8x0           49152  2
intel_rapl_msr         20480  0
--snip--
````

---


### 3.
Enable IP forwarding with a `sysctl` command.

---

````shell
┌──(root💀Kali)-[/]
└─#  sysctl -w net.ipv4.ip_forward=1                                                                                                                   1 ⚙
net.ipv4.ip_forward = 1

````

---


### 4.
Edit your `/etc/sysctl.conf` file to enable IP forwarding. Now, disable IP forwarding.

---

````shell
┌──(root💀Kali)-[/]
└─# vi /etc/sysctl.conf

````

---


### 5.
Select one kernel module and learn more about it using `modinfo`.

---

````shell
┌──(root💀Kali)-[/]
└─# modinfo bluetooth
filename:       /lib/modules/5.7.0-kali1-amd64/kernel/net/bluetooth/bluetooth.ko
alias:          net-pf-31
license:        GPL
version:        2.22
description:    Bluetooth Core ver 2.22
author:         Marcel Holtmann <marcel@holtmann.org>
srcversion:     10CFBB471D0159F7D6CBD34
depends:        libaes,rfkill,ecdh_generic,crc16
retpoline:      Y
intree:         Y
name:           bluetooth
vermagic:       5.7.0-kali1-amd64 SMP mod_unload modversions
parm:           disable_esco:Disable eSCO connection creation (bool)
parm:           disable_ertm:Disable enhanced retransmission mode (bool)
parm:           enable_ecred:Enable enhanced credit flow control mode (bool)
````

---
