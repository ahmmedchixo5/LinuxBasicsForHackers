<!---
  Name          : Chapter_7.md
  Project       : Linux Basics for Hackers 
  Description   : Solutions to chapter 7 exercise problems

--->


# Chapter 7 Exercise Problems

### 1.
View all of your environment variables with the `more` command.

---

````shell
k┌──(root💀Kali)-[/]
└─#  set | more                                                                                                                                  127 ⨯ 1 ⚙
'!'=0
'#'=0
'$'=3350
'*'=(  )
-=3569JXghiks
0=zsh
'?'=127
@=(  )
ARGC=0
CDPATH=''
COLUMNS=155
CPUTYPE=x86_64
DISPLAY=:0.0
EGID=0
EUID=0
FIGNORE=''

--snip--

````

---


### 2.
Use the `echo` command to view the `HOSTNAME` variable.

---

````shell
┌──(root💀Kali)-[/]
└─#  echo $HOSTNAME                                                                                                                                                     
kali
````

---


### 3.
Find a method to change the slash (`/`) to a backslash ('\') in the faux Microsoft `cmd PS1` example (see Listing 7.2).

---

````shell
┌──(root💀Kali)-[/]
└─#  PS1='C:\\\W> '
C:\\W> cd /home  
C:\\W> ls 
ahmed

to out from this mode use commend exit 
````

---


### 4.
Create a variable names `MYNEWVARIABLE` and put your name in it.

---

````shell
┌──(ahmed㉿Kali)-[~]
└─$ MYNEWVARIABLE=ahmed

````

---


### 5.
Use `echo` to view the contents of `MYNEWVARIABLE`.

---

````shell
┌──(ahmed㉿Kali)-[~]
└─$ echo $MYNEWVARIABLE
ahmed
            
````

---


### 6.
Export `MYNEWVARIABLE` so that it's available in all environments.

---

````shell
┌──(ahmed㉿Kali)-[~]
└─$ export MYNEWVARIABLE

````

---


### 7.
Use the echo command to view the contents of the `PATH` variable.

---

````shell
                                                                                                                                                           
┌──(ahmed㉿Kali)-[~]
└─$ echo $PATH                                                                                                                                     
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/games:/usr/games

````

---


### 8.
Add your home directory to the `PATH` variable so that any binaries in your home directory can be used in any directory.

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  PATH=$PATH:/home/kali
````

---


### 9.
Change your `PS1` variable to "World's Greatest Hacker:".

---

````shell
┌──(ahmed㉿Kali)-[/home]
└─$  PS1="World's Greatest Hacker: "
World's Greatest Hacker:
````

---
