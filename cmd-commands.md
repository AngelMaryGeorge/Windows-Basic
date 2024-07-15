# Comprehensive List of CMD Commands

## File and Directory Commands

### dir : Lists the contents of a directory.

```shell
dir
```
Example:
```shell
dir C:\Users
```

### cd : Changes the current directory.

```shell
cd <directory>
```
Example:
```shell
cd C:\Windows\System32
```

### md or mkdir : Creates a new directory.
```shell
md <directory>
mkdir <directory>
```
Example:

```shell
mkdir C:\NewFolder
```

### rd or rmdir : Removes an empty directory.
```shell
rd <directory>
rmdir <directory>
```
Example:
```shell
rmdir C:\OldFolder
```

### del or erase : Deletes one or more files.
```shell
del <file>
erase <file>
```
Example:
```shell
del C:\temp\oldfile.txt
```

### copy : Copies one or more files to another location.
```shell
copy <source> <destination>
```
Example:
```shell
copy C:\file.txt D:\backup\file.txt
```

### move : Moves one or more files from one directory to another.
```shell
move <source> <destination>
```
Example:
```shell
move C:\file.txt D:\backup\file.txt
```

### rename or ren : Renames a file or directory.
```shell 
rename <oldname> <newname>
ren <oldname> <newname>
```
Example:
```shell
 rename C:\file.txt newfile.txt
```

### xcopy : Copies files and directory trees.
```shell
 xcopy <source> <destination> [options]
```
Example:
```shell
 xcopy C:\source D:\destination /E /H /C /I
```

## System Information Commands

### systeminfo : Displays detailed configuration information about a computer and its operating system.
```shell
 systeminfo
```

### hostname : Displays the hostname of the computer.
```shell
 hostname
```

### tasklist : Displays a list of currently running processes on the local or a remote computer.
```shell
tasklist
```

### taskkill : Ends one or more tasks or processes.
```shell
taskkill /F /IM <processname>
```
Example:
```shell 
taskkill /F /IM notepad.exe
```

### chkdsk : Checks a disk and displays a status report.
```shell
chkdsk [volume] [options]
```
Example:
```shell
 chkdsk C: /F /R
```

## Network Commands

### ipconfig : Displays all current TCP/IP network configuration values and refreshes Dynamic Host Configuration Protocol (DHCP) and Domain Name System (DNS) settings.
```shell
ipconfig
```

### ping : Sends ICMP Echo Requests to network hosts.
```shell
ping <hostname or IP address>
```
Example:
```shell
ping google.com
```

### tracert : Traces the route to a remote host.
```shell
tracert <hostname or IP address>
```
Example:
```shell 
tracert google.com
```

### netstat : Displays network connections, routing tables, and a number of network interface statistics.
```shell
netstat
```

### nslookup : Queries the DNS to obtain domain name or IP address mapping or any other specific DNS record.
```shell
nslookup <hostname>
```
Example:
```shell
 nslookup google.com
```

## Disk Management Commands

### diskpart : Opens the Disk Partition command interpreter.
```shell
diskpart
```

### format : Formats a disk for use with Windows.
```shell
format <volume> [options]
```
Example:
```shell
format D: /FS:NTFS
```

### diskcopy : Copies the contents of one floppy disk to another.
```shell
 diskcopy <drive1> <drive2>
```
Example:
```shell
 diskcopy A: B:
```

## User and Group Management Commands

### net user : Adds, deletes, and displays user accounts.
```shell
net user [username [password | *] [options]] [/domain]
```
Example:
```shell
net user johndoe Pa$$w0rd /add
```

### net localgroup : adds, displays, or modifies local groups.
```shell
net localgroup [groupname [username [ ...]] [/add | /delete]]
```
Example:
```shell
net localgroup administrators johndoe /add
```

## Miscellaneous Commands

### cls : Clears the screen.
```shell 
cls
```

### echo : Displays messages, or turns command echoing on or off.
```shell 
echo [message]
```
Example:
```shell
echo Hello, World!
```

### pause: Suspends processing of a batch file and displays a message.
```shell
pause
```

### shutdown : Shuts down or restarts the computer.
```shell
shutdown [options]
```
Example:
```shell
shutdown /s /t 0
```

### type : Displays the contents of a text file.
```shell
type <filename>
```
Example:
```shell
type C:\example.txt
```

### attrib : Displays or changes file attributes.
```shell 
attrib [options] <filename>
```
Example:
```shell 
attrib +r C:\example.txt
```

### find : Searches for a text string in a file or files.
```shell
find "<string>" <filename>
```
Example:
```shell
find "Hello" C:\example.txt
```

### fc : Compares two files and displays the differences.
```shell 
fc <file1> <file2>
```
Example:
```shell 
fc C:\file1.txt C:\file2.txt
```

### replace : Replaces files.
```shell 
replace <source> <destination> [options]
```
Example:
```shell 
replace C:\newfile.txt D:\backup\
```

### date : Displays or sets the date.
```shell 
date [date]
```
Example:
```shell 
date 12-31-2024
```

### time : Displays or sets the system time.
```shell
time [time]
```
Example:
```shell
time 23:59
```

### color : Sets the default console foreground and background colors.
```shell 
color [attr]
```
Example:
```shell
color 0A
```

### title : Sets the window title for the CMD session.
```shell
title [string]
```
Example:
```shell 
title My Command Prompt
```

### ver : Displays the Windows version.
```shell
ver
```

### set : Displays, sets, or removes environment variables.
```shell
set [variable=[string]]
```
Example:
```shell 
set PATH=C:\Windows\System32
```
