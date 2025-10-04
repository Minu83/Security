

(root㉿INE)-[~]
└─# gobuster dir -u http://192.178.51.3 -w /usr/share/wordlists/dirb/common.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.178.51.3
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.htpasswd            (Status: 403) [Size: 288]
/ajax                 (Status: 301) [Size: 310] [--> http://192.178.51.3/ajax/]
/.htaccess            (Status: 403) [Size: 288]
/.hta                 (Status: 403) [Size: 283]
/.git/HEAD            (Status: 200) [Size: 23]
/cgi-bin/             (Status: 403) [Size: 287]
/classes              (Status: 301) [Size: 313] [--> http://192.178.51.3/classes/]
/config               (Status: 301) [Size: 312] [--> http://192.178.51.3/config/]
/data                 (Status: 301) [Size: 310] [--> http://192.178.51.3/data/]
/documentation        (Status: 301) [Size: 319] [--> http://192.178.51.3/documentation/]
/images               (Status: 301) [Size: 312] [--> http://192.178.51.3/images/]
/includes             (Status: 301) [Size: 314] [--> http://192.178.51.3/includes/]
/javascript           (Status: 301) [Size: 316] [--> http://192.178.51.3/javascript/]
/index.php            (Status: 200) [Size: 52756]
/LICENSE              (Status: 200) [Size: 10273]
/passwords            (Status: 301) [Size: 315] [--> http://192.178.51.3/passwords/]
/phpmyadmin           (Status: 301) [Size: 316] [--> http://192.178.51.3/phpmyadmin/]
/robots.txt           (Status: 200) [Size: 190]
/phpinfo.php          (Status: 200) [Size: 82100]
/server-status        (Status: 403) [Size: 292]
/styles               (Status: 301) [Size: 312] [--> http://192.178.51.3/styles/]
/test                 (Status: 301) [Size: 310] [--> http://192.178.51.3/test/]
/webservices          (Status: 301) [Size: 317] [--> http://192.178.51.3/webservices/]
Progress: 4614 / 4615 (99.98%)
===============================================================
Finished
===============================================================

┌──(root㉿INE)-[~]
└─# gobuster dir -u http://192.178.51.3 -w /usr/share/wordlists/dirb/common.txt -b 403,404                                                                                                 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.178.51.3
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   403,404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.git/HEAD            (Status: 200) [Size: 23]
/ajax                 (Status: 301) [Size: 310] [--> http://192.178.51.3/ajax/]
/classes              (Status: 301) [Size: 313] [--> http://192.178.51.3/classes/]
/config               (Status: 301) [Size: 312] [--> http://192.178.51.3/config/]
/data                 (Status: 301) [Size: 310] [--> http://192.178.51.3/data/]
/documentation        (Status: 301) [Size: 319] [--> http://192.178.51.3/documentation/]
/images               (Status: 301) [Size: 312] [--> http://192.178.51.3/images/]
/includes             (Status: 301) [Size: 314] [--> http://192.178.51.3/includes/]
/javascript           (Status: 301) [Size: 316] [--> http://192.178.51.3/javascript/]
/LICENSE              (Status: 200) [Size: 10273]
/index.php            (Status: 200) [Size: 52756]
/passwords            (Status: 301) [Size: 315] [--> http://192.178.51.3/passwords/]
/phpmyadmin           (Status: 301) [Size: 316] [--> http://192.178.51.3/phpmyadmin/]
/phpinfo.php          (Status: 200) [Size: 82101]
/robots.txt           (Status: 200) [Size: 190]
/styles               (Status: 301) [Size: 312] [--> http://192.178.51.3/styles/]
/test                 (Status: 301) [Size: 310] [--> http://192.178.51.3/test/]
/webservices          (Status: 301) [Size: 317] [--> http://192.178.51.3/webservices/]
Progress: 4614 / 4615 (99.98%)
===============================================================
Finished
===============================================================

┌──(root㉿INE)-[~]
└─# gobuster dir -u http://192.178.51.3 -w /usr/share/wordlists/dirb/common.txt -b 403,404  -x .php,.txt,.xml -r
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.178.51.3
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   403,404
[+] User Agent:              gobuster/3.6
[+] Extensions:              php,txt,xml
[+] Follow Redirect:         true
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.git/HEAD            (Status: 200) [Size: 23]
/ajax                 (Status: 200) [Size: 965]
/classes              (Status: 200) [Size: 3663]
/config               (Status: 200) [Size: 740]
/credits.php          (Status: 500) [Size: 30]
/data                 (Status: 200) [Size: 941]
/documentation        (Status: 200) [Size: 2620]
/home.php             (Status: 500) [Size: 46]
/images               (Status: 200) [Size: 10180]
/includes             (Status: 200) [Size: 4506]
/installation.php     (Status: 200) [Size: 7701]
/index.php            (Status: 200) [Size: 52756]
/index.php            (Status: 200) [Size: 52756]
/javascript           (Status: 200) [Size: 1981]
/LICENSE              (Status: 200) [Size: 10273]
/login.php            (Status: 500) [Size: 1205]
/page-not-found.php   (Status: 200) [Size: 241]
/passwords            (Status: 200) [Size: 948]
/phpmyadmin.php       (Status: 200) [Size: 157]
/phpinfo.php          (Status: 200) [Size: 82101]
/phpinfo.php          (Status: 200) [Size: 82101]
/register.php         (Status: 500) [Size: 0]
/phpmyadmin           (Status: 200) [Size: 2736]
/robots.txt           (Status: 200) [Size: 190]
/robots.txt           (Status: 200) [Size: 190]
/styles               (Status: 200) [Size: 1354]
/test                 (Status: 200) [Size: 938]
/webservices          (Status: 200) [Size: 1320]
Progress: 18456 / 18460 (99.98%)
===============================================================
Finished
===============================================================

┌──(root㉿INE)-[~]
└─# gobuster dir -u http://192.178.51.3/data -w /usr/share/wordlists/dirb/common.txt -b 403,404  -x .php,.txt,.xml -r                                                                      
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.178.51.3/data
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   403,404
[+] User Agent:              gobuster/3.6
[+] Extensions:              txt,xml,php
[+] Follow Redirect:         true
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/accounts.xml         (Status: 200) [Size: 3679]
Progress: 18456 / 18460 (99.98%)
===============================================================
Finished
===============================================================
