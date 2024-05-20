
Nmap [IP] [options] //scanare porturi, service versions, OS

Tar -xf [filename].tar.gz //decompress tar files

Nc -nvlp [port] //listener session open. Use some port that is not used frequently e.g 1234

ls -al /usr/share/nmap/scripts/ | grep ftp-*  // how to check for nmap scripts. Replace ftp with what you want to look for

Searchsploit proftpd // search for exploits by service version name

ffuf -u [http://]ip]/FUZZ](http://]ip]/FUZZ) -w [path]  //directory and  subdomain enumeration

find / -perm -u=s -type f 2>/dev/null  //find SUID files

find / -perm /4000 2> /dev/null  //find SUID files

getcap -r / 2>/dev/null

gobuster dir -u [http://192.210.78.3](http://192.210.78.3) -w /usr/share/wordlists/dirb/common.txt

smbclient //host_name/share_name -U " "%" "

We can use the getcap tool to list enabled capabilities:
getcap -r / 2>/dev/null


**==Stabilizare shell:==**

python3 -c 'import pty;pty.spawn("/bin/bash")'
export TERM=xterm
Ctrl+z // put in background
stty raw -echo; fg