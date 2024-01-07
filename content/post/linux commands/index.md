---
title: Linux commands for network engineers
date: 2023-12-20
description: Essential Linux commands
draft: false
tags: 
    - linux
    - 101
categories:
    - linux
image: linux.png
---

**ls**: 
Lists directories and files in the current directory.  
Example:  

    ubuntu@panda:~$ ls
    clab     docker-compose  downloads  hugo     package-lock.json  scripts
    compose  docker-vol      service    lasthop  powerlevel10k      tf

**pwd**:
Prints the current working directory.  
Example:

    ubuntu@panda:~$ pwd
    /home/ubuntu

**cd**:
Navigate through directories.  
Example:

    ubuntu@panda:~$ cd clab
    ubuntu@panda:~/clab$ cd
    ubuntu@panda:~$ 

**mkdir**:
Create directories.  
Example:

    ubuntu@panda:~$ mkdir newdir
    ubuntu@panda:~$ ls
    clab     docker-compose  downloads  hugo     newdir             powerlevel10k  tf
    compose  docker-vol      service    lasthop  package-lock.json  scripts

**mv**:
Move or rename files.  
Example:

    ubuntu@panda:~$ mv downloads downloads_backup
    ubuntu@panda:~$ ls
    clab     docker-compose  downloads_backup  hugo     package-lock.json  scripts
    compose  docker-vol      service           lasthop  powerlevel10k      tf

**cp**:
Copy files.  
Example:

    ubuntu@panda:~$ cp package-lock.json package-lock-backup.json
    ubuntu@panda:~$ ls
    clab     docker-compose  downloads  hugo     package-lock-backup.json  package-lock.json  powerlevel10k  scripts
    compose  docker-vol      service    lasthop  tf

**rm**:
Delete files or directories.  
Example:

    ubuntu@panda:~$ rm package-lock-backup.json
    ubuntu@panda:~$ ls
    clab     docker-compose  downloads  hugo     package-lock.json  powerlevel10k  scripts
    compose  docker-vol      service    lasthop  tf

**touch**:
Create blank/empty files.  
Example:

    ubuntu@panda:~$ touch newfile.txt
    ubuntu@panda:~$ ls
    clab     docker-compose  downloads  hugo     newfile.txt          package-lock.json  powerlevel10k  scripts
    compose  docker-vol      service    lasthop  tf


**cat**:
Display file contents on the terminal.  
Example:

    ubuntu@panda:~$ cat newfile.txt 
    hello world

**clear**:
Clear the terminal display.  
Example:

    ubuntu@panda:~$ clear

**echo**:
Print any text that follows the command.  
Example:

    ubuntu@panda:~$ echo "hello world"
    hello world

**less**:
Display paged outputs in the terminal.  
Example:

    ubuntu@panda:~$ less package-lock.json

**man**:
Access manual pages for Linux commands.  
Example:

    ubuntu@panda:~$ man ls

**uname**:
Get basic information about the OS.  
Example:

    ubuntu@panda:~$ uname -a
    Linux panda 5.15.0-1049-oracle

**whoami**:
Get the active username.  
Example:

    ubuntu@panda:~$ whoami
    ubuntu

**tar**:
Extract and compress files.  
Example:

    ubuntu@panda:~$ tar -xvf archive.tar

**grep**:
Search for a string within an output.  
Example:

    ubuntu@panda:~$ grep "pattern" filename

**head**:
Return the specified number of lines from the top.  
Example:

    ubuntu@panda:~$ head -n 5 filename

**tail**:
Return the specified number of lines from the bottom.  
Example:

    ubuntu@panda:~$ tail -n 5 filename

**diff**:
Find the difference between two files.  
Example:

    ubuntu@panda:~$ diff file1 file2

**cmp**:
Check if two files are identical.  
Example:

    ubuntu@panda:~$ cmp file1 file2

**comm**:
Combine the functionality of diff and cmp.  
Example:

    ubuntu@panda:~$ comm file1 file2

**sort**:
Sort the content of a file while outputting.  
Example:

    ubuntu@panda:~$ sort filename

**export**:
Export environment variables.  
Example:

    ubuntu@panda:





**ps**:
Display active processes.  
Example:

    ubuntu@panda:~$ ps
    PID TTY          TIME CMD
    1234 pts/1    00:00:01 bash
    5678 pts/1    00:00:03 python

**kill** and **killall**:
Kill active processes by process ID or name.  
Example:

    ubuntu@panda:~$ kill 1234
    ubuntu@panda:~$ killall python

**df**:
Display disk filesystem information.  
Example:

    ubuntu@panda:~$ df -h
    Filesystem      Size  Used Avail Use% Mounted on
    /dev/sda1       20G  15G  4.0G  80% /


**chmod**:
Change file permissions.  
Example:

    ubuntu@panda:~$ chmod 755 script.sh
    ubuntu@panda:~$ ls -l script.sh
    -rwxr-xr-x 1 ubuntu ubuntu 0 Jan  1 12:00 script.sh

**chown**:
Grant ownership of files or folders.  
Example:

    ubuntu@panda:~$ chown ubuntu:ubuntu script.sh
    ubuntu@panda:~$ ls -l script.sh
    -rwxr-xr-x 1 ubuntu ubuntu 0 Jan  1 12:00 script.sh

**ifconfig**:
Display network interfaces and IP addresses.  
Example:

    ubuntu@panda:~$ ifconfig
    eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
            inet 192.168.1.2  netmask 255.255.255.0  broadcast 192.168.1.255

**traceroute**:
Trace all the network hops to reach the destination.  
Example:

    ubuntu@panda:~$ traceroute google.com

**wget**:
Direct download files from the internet.  
Example:

    ubuntu@panda:~$ wget https://example.com/file.zip




**cal**:
View a command-line calendar.  
Example:

    ubuntu@panda:~$ cal
       January 2023      
    Su Mo Tu We Th Fr Sa  
                    1   
    2  3  4  5  6  7  8   
    9 10 11 12 13 14 15  
    16 17 18 19 20 21 22  
    23 24 25 26 27 28 29  
    30 31                

**alias**:
Create custom shortcuts for regularly used commands.  
Example:

    ubuntu@panda:~$ alias ll='ls -l'
    ubuntu@panda:~$ ll
    total 4
    drwxrwxr-x 2 ubuntu ubuntu 4096 Jan  1 12:00 clab

**dd**:
Majorly used for creating bootable USB sticks.  
Example:

    ubuntu@panda:~$ sudo dd if=/path/to/iso of=/dev/sdb bs=4M status=progress

**whereis**:
Locate the binary, source, and manual pages for a command.  
Example:

    ubuntu@panda:~$ whereis ls
    ls: /bin/ls /usr/share/man/man1/ls.1.gz

**whatis**:
Find what a command is used for.  
Example:

    ubuntu@panda:~$ whatis ls
    ls (1) - list directory contents

**top**:
View active processes live with their system usage.  
Example:

    ubuntu@panda:~$ top

**useradd** and **usermod**:
Add new user or change existing users' data.  
Example:

    ubuntu@panda:~$ sudo useradd newuser
    ubuntu@panda:~$ sudo usermod -aG sudo newuser

**passwd**:
Create or update passwords for existing users.  
Example:

    ubuntu@panda:~$ sudo passwd newuser
    Enter new UNIX password: 
    Retype new UNIX password: 
    passwd: password updated successfully

**ls -1 | wc -l**:
Get the count of the files present in a directory.  
Example:

    ubuntu@panda:~$ ls -1 | wc -l
    12

**kill**:
Command to kill a process (PID).  
Example:

    ubuntu@panda:~$ kill 1234

**w**:
Check how many users are logged into Linux.  
Example:

    ubuntu@panda:~$ w
     12:00:00 up 10 days,  2:00,  2 users,  load average: 0.00, 0.01, 0.05

**date**:
Used to check the current date and time in Linux.  
Example:

    ubuntu@panda:~$ date
    Sat Jan  1 12:00:00 UTC 2023

**ls -a**:
List the hidden files in a directory.  
Example:

    ubuntu@panda:~$ ls -a
    .  ..  .hiddenfile  clab  downloads

**ls -l**:
Check the permissions on all the files.  
Example:

    ubuntu@panda:~$ ls -l
    total 4
    drwxrwxr-x 2 ubuntu ubuntu 4096 Jan  1 12:00 clab

**ls -R**:
List information about files and directories within the file system.  
Example:

    ubuntu@panda:~$ ls -R
    .:
    clab  downloads

    ./clab:
    file1  file2

    ./downloads:
    file3  file4

**rm -rf**:
Remove directory with the files.  
Example:

    ubuntu@panda:~$ rm -rf old_directory
    ubuntu@panda:~$ ls
    clab  downloads
