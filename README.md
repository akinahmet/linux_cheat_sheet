DevOps ve Networking İçin  Linux Komutları [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
===============
<hr>
<p align="center">
	<img alt="Git" src="./Img/linux.svg" height="190" width="455">
</p>
<hr>

### Index
* [lsof Command](#lsof_command)
* [Groups and Users](#groups_and_users)
* [id Command](#id_command)
* [cat Command](#cat_command)
* [diff Command](#diff_command)
* [dd Command](#dd_command)
* [route Command](#route_command)
* [mtr Command](#mtr_command)
* [nslookup ve dig Commands](#nslookup_ve_dig_commands)
* [tcpdump Command](#tcpdump_command)
* [sudo !! Command](#sudo_!!_command)
* [wget Command](#wget_command)
* [free Command](#free_command)
* [tr Command](#tr_command)
* [htop, ps ve kill Commands](#htop_ps_ve_kill_commands)
* [head and tail Commands](#head_and_tail_commands)
* [man Command](#man_command)
* [sort Command](#sort_command)
* [chown Command](#chown_command)
* [chmod Command](#chmod_command)

<hr>

## lsof Command 
##### lsof command stands for List Of Open File.

##### This command provides a list of files that are opened.:
```
lsof -u “user”
```

<hr>

## Groups and Users

##### We use this command to create new users.:
```
sudo useradd “username”
```

##### The passwd command changes passwords for user accounts.:
```
sudo passwd “username” 
```

##### Delete a user account and related files:
```
sudo userdel “username” 
```

##### We use groupadd command to create a new user group.:
```
sudo groupadd “groupname” 
```

##### groupdel command is used to delete a existing group.:
```
sudo groupdel “groupname” 
```

##### This command adds a user to a group.:
```
sudo usermod -g “groupname” “username” 
```

<hr>

## id Command
##### (This command is used to find out user and group names and numeric ID’s of the current user or any other user in the server.)

##### Print only the effective group id:
```
id -g 
```

##### Print all Group ID’s:
```
id -G
```

##### Prints only the effective user ID:
```
id -u 
```

<hr>

## cat Command
##### ( It reads data from the file and gives their content as output. It helps us to create, view, concatenate files.)

##### This will show the content of test1.txt and test2.txt:
```
cat “test-1.txt” “test-2.txt” 
```

##### Number nonempty output lines:
```
cat -b 
```

##### Number all output lines:
```
cat -n 
```

<hr>

## diff Command

##### To compare the content of two files line by line:
```
diff “test-1.txt” “test-2.txt”
```

<hr>

## dd Command
##### (This tool is mainly used for copying and converting data, hence it stands for data duplicator.  This tool can be also used for: Backing up and restoring an entire hard drive or a partition.Create .ISO from CD/DVD)

##### To copy Mountpoint1 to Mountpoint2 :
```
dd if = /dev/mp1 of = /dev/mp2 
```


##### If there are read errors while reading the source, we use conv=sync,noerror to prevent dd from stopping on error and performing a dump-:
```
dd conv=noerror if = /dev/mp1 of = /dev/mp2
```

<hr>

## route Command

##### Route command is used to show/manipulate the IP routing table.:
```
route
```

##### traceroute command in Linux prints the route that a packet takes to reach the host.:
```
traceroute google.com
```

<hr>

## mtr Command
##### (Mtr(my traceroute) is a command line network diagnostic tool that provides the functionality of both the ping and traceroute commands.)

##### View traceroute report in real time:
```
mtr google.com 
```

##### It only throws 10 packets at the target and lists the result as a report. The -n parameter blocks DNS resolution:
```
mtr -n --report google.com
```

<hr>

## nslookup ve dig Commands

##### Sorts the NS and SOA records of the given address:
```
nslookup github.com
```
```
dig google.com
```

<hr>

## tcpdump Command
##### (It queries the status of all network interfaces on the machine and captures the packets sent from the interfaces.)

##### Lists all interfaces:
```
sudo tcpdump --list-interfaces
```

##### To capture the packets of current network interface:
```
sudo tcpdump
```

##### To capture packets from a specific network interface:
```
sudo tcpdump -i eth0
```

##### To capture specific number of packets:
```
sudo tcpdump -i eth0 -c 10 
```

<hr>

## sudo !! Command

##### This command repeats the command previously entered on the command line with root privileges:
```
sudo !!
```

<hr>

## wget Command

##### This command will download the resource specified in the [url] to the current directory.:
```
wget https://www.linkedin.com/in/mahmut-edip-negiz-6b1145213/
```

<hr>

## free Command

##### Command will shows below memory information. Running it without an option will show you a default view with kilobyte units.:
```
free
```

##### view with bytes :
```
free -b
```

#####  view with kilobytes (default):
```
free -k
```

##### view with megabytes :
```
free -m
```

##### view with gigabytes :
```
free -g
```

<hr>

## tr Command
##### (The ‘tr’ in tr command stands for translation. This command is used for translating one type of characters into another. )

##### convert all 'e's in text to 'o':
```
cat deneme.txt | tr “e” “o” 
```

#####  convert lowercase to uppercase:
```
cat deneme.txt | tr “[a-z]” “[A-Z]”
```

#####  to delete spesific character(s) :
```
cat deneme.txt | tr -d “i” 
```

<hr>

## htop, ps and kill Commands

##### htop is a linux application used for real-time process (cpu and memory) monitoring.:
```
htop
```

#####  ps is used for real-time process (cpu and memory) monitoring too. The difference is reporting the output:
```
ps aux

a = Shows the transactions of all users.
u = Displays the owner of the action.
x = Displays processes not connected to the terminal.
```

#####  The kill command will kill a single process at a time with the given process ID. :
```
kill “ID”
```

<hr>

## head and tail Commands

#####  The 'head' command displays the starting content of a file. By default, it displays starting 10 lines of any file:
```
head “file.txt” 
```

##### The Linux tail command displays data from the end of a file.:
```
tail “file.txt”  
```

<hr>

## whoAMI Command

##### It displays the username of the current user when this command is invoked:
```
whoami
```

<hr>

## sort Command
##### (The sort command arranges text lines in useful ways. This simple tool can help you quickly sort information from the command line.)

##### Sort in reverse order:
```
sort -r
```

##### Ignore case while sorting:
```
sort -f 
```

##### Sort on numerical value:
```
sort -n
```

<hr>

## chown Command

##### Change ownership of files:
```
sudo chown “user_or_group_name” “file_name”
```

<hr>

## chmod Command

##### This command is used to change the access permissions of files and directories. Each digit represents user, group, and others:
```
chmod 754 “file.txt”

4 →read(r) permission
2 → write(w) permission
1 → execute(x) permission
0 → no permission
```
