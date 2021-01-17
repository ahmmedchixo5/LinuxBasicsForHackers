<!---
  Name          : Chapter_6.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 6 exercise problems

--->


# Chapter 6 Exercise Problems

### 1.
Run the `ps` command with the `aux` options on your system and note which process is first and which is last.

---

````shell
┌──(root💀Kali)-[/]
└─# ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.1 168104 11188 ?        Ss   12:53   0:02 /sbin/init splash
root           2  0.0  0.0      0     0 ?        S    12:53   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   12:53   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   12:53   0:00 [rcu_par_gp]
root           6  0.0  0.0      0     0 ?        I<   12:53   0:00 [kworker/0:0H-kblockd]
root           7  0.0  0.0      0     0 ?        I    12:53   0:00 [kworker/0:1-mm_percpu_wq]
root           9  0.0  0.0      0     0 ?        I<   12:53   0:00 [mm_percpu_wq]
root          10  0.0  0.0      0     0 ?        S    12:53   0:00 [ksoftirqd/0]
root          11  0.0  0.0      0     0 ?        I    12:53   0:03 [rcu_sched]
root          12  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/0]
root          13  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/0]
root          14  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/1]
root          15  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/1]
root          16  0.0  0.0      0     0 ?        S    12:53   0:00 [ksoftirqd/1]
root          17  0.0  0.0      0     0 ?        I    12:53   0:00 [kworker/1:0-events]
root          18  0.0  0.0      0     0 ?        I<   12:53   0:00 [kworker/1:0H-kblockd]
root          19  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/2]
root          20  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/2]
root          21  0.0  0.0      0     0 ?        S    12:53   0:00 [ksoftirqd/2]
root          23  0.0  0.0      0     0 ?        I<   12:53   0:00 [kworker/2:0H-kblockd]
root          24  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/3]
root          25  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/3]
root          26  0.0  0.0      0     0 ?        S    12:53   0:00 [ksoftirqd/3]
root          28  0.0  0.0      0     0 ?        I<   12:53   0:00 [kworker/3:0H-kblockd]
root          29  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/4]
root          30  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/4]
root          31  0.0  0.0      0     0 ?        S    12:53   0:00 [ksoftirqd/4]
root          33  0.0  0.0      0     0 ?        I<   12:53   0:00 [kworker/4:0H]
root          34  0.0  0.0      0     0 ?        S    12:53   0:00 [cpuhp/5]
root          35  0.0  0.0      0     0 ?        S    12:53   0:00 [migration/5]
--snip--
````

---


### 2.
Run the `top` command and note the two processes using the greatest amount of your resources.

---

````shell
┌──(root💀Kali)-[/]
└─# top
  PID  USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                             
  591  root      20   0 1191540 107264  46696 S   4.0   1.2   0:50.37 Xorg                                                                                
  1125 ahmed     20   0  199960  22540  16852 S   1.7   0.3   1:08.03 panel-22-cpugra                                                                     
  1304 ahmed     20   0 1305572  94480  72580 S   1.3   1.1   0:19.40 qterminal                                                                           
  855  ahmed     20   0  275396  23728  17292 S   0.3   0.3   0:00.35 xfce4-session
  --snip--  
````

---


### 3.
Use the `kill` command to kill the process that uses the most resources.

---

````shell
┌──(root💀Kali)-[/]
└─#  kill 10883 
````

---


### 4.
Use the `renice` command to reduce the priority of a running process to `+19`.

---

````shell
┌──(root💀Kali)-[/]
└─# renice 19 10902  
10902 (process ID) old priority 0, new priority 19
````

---


### 5.
Create a script called `myscanning` (to see how to write a bash script, see Chapter 8; the content of the script is not important) with a text editor and then schedule it to run next Wednesday at `1 AM`.

---

````shell
──(root💀Kali)-[/]
└─# at 1:00am 20/01/2021 
warning: commands will be executed using /bin/sh
at> /home/ahmed/myscanning
````

---
