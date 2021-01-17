<!---
  Name          : Chapter_3.md
  Project       : Linux Basics for Hackers 1e
  Description   : Solutions to chapter 3 exercise problems
--->


# Chapter 3 Exercise Problems

### 1.
Find information on your active network interfaces.

---

````shell
┌──(root💀Kali)-[/]
└─# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:fee7:3053  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:e7:30:53  txqueuelen 1000  (Ethernet)
        RX packets 4  bytes 780 (780.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 16  bytes 1518 (1.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 12  bytes 556 (556.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 12  bytes 556 (556.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

````

---


### 2.
Change the IP address on `eth0` to `192.168.1.1`.

---

````shell
┌──(root💀Kali)-[/]
└─#  ifconfig eth0 194.168.1.1/24 

┌──(root💀Kali)-[/]
└─# ifconfig                     
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 194.168.1.1  netmask 255.255.255.0  broadcast 194.168.1.255
        inet6 fe80::a00:27ff:fee7:3053  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:e7:30:53  txqueuelen 1000  (Ethernet)
        RX packets 4  bytes 780 (780.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 16  bytes 1518 (1.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 12  bytes 556 (556.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 12  bytes 556 (556.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

````

---


### 3.
Change your hardware address on `eth0`.

---

````shell
                                                                                                                                                           
┌──(root💀Kali)-[/]
└─#  ifconfig eth0 down
                                                                                                                                                           
┌──(root💀Kali)-[/]
└─#  ifconfig eth0 hw ether 00:11:22:33:44:55
                                                                                                                                                           
┌──(root💀Kali)-[/]
└─#  ifconfig eth0 up
                                                                                                                                                           
┌──(root💀Kali)-[/]
└─#  ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 194.168.1.1  netmask 255.255.255.0  broadcast 194.168.1.255
        inet6 fe80::211:22ff:fe33:4455  prefixlen 64  scopeid 0x20<link>
        ether 00:11:22:33:44:55  txqueuelen 1000  (Ethernet)
        RX packets 20033  bytes 22783016 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9756  bytes 763389 (745.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141073  bytes 16696314 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141073  bytes 16696314 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
````

---


### 4.
Check whether you have any available wireless interfaces active.

---

````shell
┌──(root💀Kali)-[/]
└─# iwconfig                                                                                                                                         127 ⨯
lo        no wireless extensions.

eth0      no wireless extensions.

````

---


### 5.
Reset your IP address to a DHCP-assigned address.

---

````shell
root@kali:/home/kali# dhclient eth0
root@kali:/home/kali# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.16.194.132  netmask 255.255.255.0  broadcast 172.16.194.255
        inet6 fe80::211:22ff:fe33:4455  prefixlen 64  scopeid 0x20<link>
        ether 00:11:22:33:44:55  txqueuelen 1000  (Ethernet)
        RX packets 20045  bytes 22784936 (21.7 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9764  bytes 764752 (746.8 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 141093  bytes 16702920 (15.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 141093  bytes 16702920 (15.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
````

---


### 6.
Find the nameserver and email server of your favorite website.

---

````shell
┌──(root💀Kali)-[/]
└─# sudo apt-get install dnsutils                                                                                                                    100 ⨯
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  bind9-dnsutils bind9-libs
The following NEW packages will be installed:
  bind9-dnsutils dnsutils
The following packages will be upgraded:
  bind9-libs


┌──(root💀Kali)-[/]
└─# dig github.com ns            

; <<>> DiG 9.16.8-Debian <<>> github.com ns
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 26503
;; flags: qr rd ra; QUERY: 1, ANSWER: 8, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1220
; COOKIE: f754e2732d6952fbabb1b11360048090de490b5693c64745 (good)
;; QUESTION SECTION:
;github.com.                    IN      NS

;; ANSWER SECTION:
github.com.             656     IN      NS      dns2.p08.nsone.net.
github.com.             656     IN      NS      ns-1283.awsdns-32.org.
github.com.             656     IN      NS      ns-520.awsdns-01.net.
github.com.             656     IN      NS      ns-1707.awsdns-21.co.uk.
github.com.             656     IN      NS      dns4.p08.nsone.net.
github.com.             656     IN      NS      ns-421.awsdns-52.com.
github.com.             656     IN      NS      dns1.p08.nsone.net.
github.com.             656     IN      NS      dns3.p08.nsone.net.

;; Query time: 32 msec
;; SERVER: 192.168.1.1#53(192.168.1.1)
;; WHEN: Sun Jan 17 13:23:12 EST 2021
;; MSG SIZE  rcvd: 290

--snip--
````

---


### 7.
Add Google's DNS server to your `/etc/resolv.conf` file so your system refers to that server when it can't resolve a domain name query with your local DNS server.

---

````shell
┌──(root💀Kali)-[/]
└─# echo "nameserver 8.8.8.8" >> /etc/resolv.conf

````

---
