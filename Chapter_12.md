<!---
  Name          : Chapter_12.md
  Project       : Linux Basics for Hackers 1e
  Description   : Solutions to chapter 12 exercise problems
--->


# Chapter 12 Exercise Problems

### 1.
Start your `apache2` service through the command line.

---

````shell
┌──(root💀Kali)-[/]
└─#  service apache2 start
````

---


### 2.
Using the `index.html` file, create a simple website announcing your arrival into the exciting world of hacking.

---

````html
<html>
<body>

<h1>Amenasec is here! </h1>

<p>ahmed has arrived into the exciting world of hacking! </p>

</body>
</html>
````

---


### 3.
Start your `SSH` service via the command line. Now connect to your Kali system from another system on your lan.

---

````shell
┌──(root💀Kali)-[/]
└─#  service ssh start
````

---


### 4.
Start your `MySQL` database service and change the root user password to `hackers-arise`. Change to the `mysql` database.

---

````shell
┌──(root💀Kali)-[/]
└─#    service mysql start
┌──(root💀Kali)-[/]
└─#    mysql -u root -p
Enter password:
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 38
Server version: 10.3.23-MariaDB-1 Debian buildd-unstable

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> use mysql
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
MariaDB [mysql]> update user set password = PASSWORD("hackers-arise") where user = 'root';
Query OK, 0 rows affected (0.003 sec)
Rows matched: 1  Changed: 0  Warnings: 0
````

---


### 5.
Start your `PostgreSQL` database service. Set it up as described in this chapter to be used by Metasploit.

---

````shell
┌──(root💀Kali)-[/]
└─#  service postgresql start
┌──(root💀Kali)-[/]
└─#  su postgres

┌──(postgres💀Kali)-[/]
└─# createuser msf_user -P
Enter password for new role:
Enter it again:
┌──(postgres💀Kali)-[/]
└─#  createdb --owner=msf_user hackers_arise_db
````

---
