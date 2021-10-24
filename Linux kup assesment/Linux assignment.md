### Ques: what is GNU project?

Ans-GNU is GNU is a recursive acronym for "GNU's Not Unix!",GNU's design is Unix-like, but differs from Unix by being free software and containing no Unix code.The GNU project is a mass collaborative initiative for the development of free software. Richard Stallman founded the project in 1978 at MIT. ... The GNU Linux project was started to create a Unix-like operating system created with source code that could be copied, modified, and redistributed.

### Ques: differennce between unix & linux

Ans-Linux refers to the kernel of the GNU/Linux operating system whereas Unix refers to the original operating system.Linux has free community support but unix has Paid commercial support.Linux has Monolithic kernel type whereas unix has various Kernel Type it can be monolithic, microkernel and hybrid.Linux`s by default shell is BASH whereas unix by default shell is bourne shell. Linux is Open source and unix is mixed. Traditionally closed source, however, few Unix projects are open source.
Linux examples are :Debian, Ubuntu, Fedora, Red Hat, Android, etc.
unix examples are :Solaris, HP-UX, Darwin, macOS X, etc.

### Another firmware than BIOS

Ans- UEFI i.e. Unified Extensible Frameware Interface

### Ques: Ques: what is UEFI? Difference bw BIOS & UEFI.

Ans-UEFI stands for Unified Extensible Firmware Interface and is the next generation interface between the operating system and platform firmware.UEFI brought to encounter the limitation of BIOS.
UEFI does the same job as a BIOS, but with one basic difference: it stores all data about initialization and startup in an .efi file, instead of storing it on the firmware.
UEFI was designed to overcome many limitations of the old BIOS, including:
UEFI supports drive sizes upto 9 zettabytes, whereas BIOS only supports 2.2 terabytes.
UEFI provides faster boot time.
UEFI has discrete driver support, while BIOS has drive support stored in its ROM, so updating BIOS firmware is a bit difficult.
UEFI offers security like "Secure Boot", which prevents the computer from booting from unauthorized/unsigned applications. 

### Ques: when should you go for ubuntu & when for other systems?

Ans-this question comes in every newcomers mind that which linux distribution should he/she use, Its totally depends on the requirement and compatibilty of the project on which you are working.

### Ques: what is linux distributions?

Ans- Different versions of linux distribution are called Distribution or distrios,these distros provide different stack, tool, and linux environment all of these are tied to linux kernel  to form a linux OS
example of Linux distribution :Debian, Ubuntu, Fedora, Red Hat, Android, etc.

### Ques: what does systemd.unit(5) means?

Ans-To check manual entry for any command use, man command_name.
If you observe carefully the above output, the top line contains systemd.unit(5), the 5 in braces is type of man entry. The number basically corresponds to section of the manual page.
The manual is split into 8 sections, which are
Section	Description
1	General Commands
2	System Calls
3	Library functions, covering in particular the C standard library
4	Special files (usually devices, those found in /dev) and drivers
5	File formats and conventions
6	Games and screensavers
7	Miscellanea
8	System administration commands and daemons



### Ques: What are getty commands and uname command?

Ans-Getty commands sets and manage the terminal command line and ports

Uname Command- Uname Command is used for displaying the information about this system.
SYNTAX- uname [option]
OPTIONS-      
•-a  It prints all the system information in the following order: 
Kernel name, network node hostname, kernel release date, kernel version, machine hardware name, hardware platform, operating system
Syntax: $uname  -a
•-s : It prints the kernel name.
Syntax: $uname  -s

•-n : It prints the hostname of the network node (current computer).
Syntax: $uname  -n

•-r :  It prints the kernel release date.
Syntax: $uname  -r

•-v :  It prints the version of the current kernel.
Syntax: $uname  -v

•-m : It prints the machine hardware name.
Syntax: $uname  -m

•-p :  It prints the type of the processor.
Syntax: $uname  -p

•-i :   It prints the platform of the hardware.
Syntax: $uname  -i

•-o :  It prints the name of the operating system.
Syntax: $uname  -a



Ques : What is squashfs file system?
Squashfs is a highly compressed read-only filesystem for Linux. It uses zlib compression to compress both files, inodes and directories. Inodes in the system are very small and all blocks are packed to minimize data overhead. Block sizes greater than 4K are supported up to a maximum of 64K.

Ques : What are /dev/loop and /dev/tty ?

> The /dev/loop devices treat files with a filesystem image as if they were block devices. 

The loop devices are snaps because snap packages are created that way.
These files were containing a filesystem that is mounted to the location. It is an approach that developers use to pack an entire package in a single file, but the operating system access all the files. The approach used here is therefore known as loop mounts.

/dev/tty is a special file, representing the terminal for the current process.

> `/dev/tty` stands for the controlling terminal (if any) for the current process. To find out which tty's are attached to which processes use the `ps -a` command at the shell prompt (command line). Look at the "tty" column.

Ques : What are Linux Signals?
A signal is an event generated by the UNIX and Linux systems in response to some condition. Upon receipt of a signal, a process may take action.
A signal is just like an interrupt; when it is generated at the user level, a call is made to the kernel of the OS, which then acts accordingly.
There are two types of signals:
Maskable: signals which can be changed or ignored by the user. 

```
e.g. Ctrl+C.
```

Non-maskable: signals which cannot be changed or ignored by the user. These typically occur when the user is signaled for non-recoverable hardware errors. 

```
Ctrl+Z
```

Ques : Purpose of creating and using hidden files.
To prevent system files or applications files for being changes accidently. These files might contain sensitive config or data and you don't want new user or any user to mess up accidently.
We can also change permission to prevent from accidental changes.

Ques : How ext4 fs is faster ?
Ext4 introduces a lot of improvements in the ways storage blocks are allocated before writing them to disk, which can significantly increase both read and write performance.


What is swap & swap memory?
Swap space is parallel space within the RAM. When there is no enough RAM space available, linux kernel takes some of the information from RAM and writes it to the swap space on the hard drive. This process is swapping process.This way, your linux system can release some RAM space and doesn't crash due to lack of memory.

Two Swap options we can use in linux


| Swap Partion                                              | Swap File                                                |
| --------------------------------------------------------- | -------------------------------------------------------- |
| Part of your hard drive                                   | A file alternate to partition                            |
| Once configured, it is not easy to change                 | You can modify the size of the swap file anytime, easily |
| Created at the time of installing your Linux distribution | Can be created after the installation.                   |


​		

Ques : how to mount a file system?
To mount a file system on device we use mount commands.

For example:

> mount [OPTION...] DEVICE_NAME DIRECTORY
>

```
sudo mount /dev/sda /media/knoldus/sachin
```

Usually when mounting a device it auto-detect common file system such as ext4 or xfs. To specify file system type use -t option

```
sudo mount -t ext4 /dev/sda /media/knoldus/Sachin
```

Ques : Mention a ZFS use case.

**ZFS(Zettabyte file system)** File system created by sun microsystems. Zfs use virtual storage pools known as storage pools that can deal with storage & management of large amounts of data. It is designed to ensure that no data cannot be lost due to physical errors or misprocessing by hardware or OS.

Ques : How to check which process running on which port?

### Using lsof command

```
lsof -i -P -n | grep -i "listen"
```

where,

- `-i` : Look for listing ports
- `-P` : Inhibits the conversion of port numbers to port names for network files.
- `-n` : Do not use DNS name

### Using netstat command

```
sudo netstat -tulpn | grep LISTEN
```

where,

- `-t` : All TCP ports
- `-u` : All UDP ports
- `-l` : display listening server
- `-p` : show PID & name
- `-n` : Don't resolves names & show ip `localhost` -> `127.0.0.1`

Ques : what is unix time sharing?

This namespace is unfortunately named by today's standards. It dates back to the early days of Unix and has to do with how information was stored for a specific system call. Today, this detail is largely lost to history and what you really need to know is that the UTS namespace allows for the segregation of hostnames. Often hostnames are simply a convenience.

Ques : what are control groups?

Cgroups are, therefore, a facility built into the kernel that allow the administrator to set resource utilization limits on any process on the system. In general, cgroups control:

- The number of CPU shares per process.
- The limits on memory per process.
- Block Device I/O per process.
- Which network packets are identified as the same type so that another application can enforce network traffic rules.

**Cgroups have four main features**

1. Resource Limiting
2. Priotizing
3. Accounting
4. Process control

Ques : difference between bin & usr/bin ?

Both are same directories. but the difference is the /usr/bin is access the super user only.

```
/bin` is symbolic link to `/usr/bin
```

Ques : Examples of awk, grep and sed

1. [awk](https://github.com/Rahul-Soni28/Linux-kup-notes/blob/master/Day-2/sed-grep-awk.md#awk)
2. sed
3. grep

###### awk

Let's create a file first

```
cat > test.txt
```

Add data in this `test.txt`

```
sachin manager account 50000
prashant clerk account 35000
ritik manager sales 50000
anmol manager account 48000
tarun peon sales 25000
deepak clerk sales 33000
sumit peon sales 23000
swastik director purchase 80000 
```

- To print lines having `account` word

```
awk '/account/{print $0}' test.txt
```

output will look like

```
sachin manager account 50000
prashant clerk account 35000
anmol manager account 48000

```

------

- To print 2nd field of file

```
awk '{print $2}' test.txt
```

Output Will look like:

```
manager
clerk
manager
manager
peon
clerk
peon
director
```

### Ques : How many tables are there in iptables?

There are five tables in iptables:

- Packet FIltering Table

  Filter Table is the default table, if there are no user defined tables this built-in table is used. The built-in chains for this tables are INPUT, OUTPUT and FORWARD.

- NAT Table

  Network Address Translation (NAT) Table is exactly what it contains, a table of network address translations; where each record in the table is a mapping of one address to another address. Typically this NAT is used for communication from private IP address to public IP address. The NAT Table has the following pre-defined chains: PREROUTING, POSTROUTING and OUTPUT.

- Mangle Table

  The Mangle table is used to alter the IP header which consists the IP address of source and destination, IP versions, segment of user data. The in-built chains that are available in this table are PREROUTING, OUTPUT, FORWARD, INPUT and POSTROUTING.

- Raw Table

  The purpose of raw table is connection tracking of the packages.

- Security Table

  This table is used for Mandatory Access Control (MAC) networking rules. Mandatory Access Control is implemented by Linux Security Modules such as SELinux.

### Ques : What is prot, opt, in, out, source & destination?

- `prot` : It denotes the protocol, for instance, tcp, udp.
- `opt`: Special options for that specific rule.
- `in`: Name of input interface via which the packet is received
- `out`: Name of output interface via which the packet will be send
- `source`: Source IP address or Domain Name
- `destination`: Destination IP address or Domain Name

 ### Ques : Why rules are added to the top?

When rules are added to the top it means a network packet will be checked against the rules serially. Now depending on the action(if it is a terminating action), if the packet matches the matching statement, the following rules are not checked and the action is executed. Otherwise the packet is checked with the following rules in the chain.

 ### Ques : What type of actions we can add to the iptables?

- `ACCEPT`: It accpets the the network packets.
- `DROP`: It rejects the the network packets.
- `REJECT`: It rejects the the network packets and sends message to the sender.

 Can we block a website by its domain name only?

Yes we can.

  ### Ques : How can we persist rules in iptables?

Persisting rules in iptables mean to store the rules in `/etc/iptables/rules.v4` or `/etc/iptables/rules.v6` such that they do not get deleted on reboot. The iptables-persistent package should be pre installed.



  ### Ques : How can we save rules in iptables?

To save the rule we need to follow the following commands:

```
sudo iptables-save > /etc/iptables/rules.v4
sudo reboot
```

 ### Ques : Difference between ufw & iptables.

| iptables                                                     | ufw                                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| iptables is a CLI tool that allows admins to configure specific rules that will enforce Linux kernel to perform actions such as accept, drop, reject, modify network packets. | UFW - Uncomplicated Firewall. It is also a firewall configuration tool implemented on top of iptables and developed to ease iptables firewall configuration. |
| To use IPtables you need to understand TCP/IP connections, more complicated protocols and it can still be complicated. | UFW provides a basic default firewall and allows you to easily turn on and off basic services. It provides a user friendly way to create an IPv4 or IPv6 host-based firewall. UFW is not as flexible but is easier to configure for common scenarios. |
| iptables is a kernel level ip filtering mechanism. It doesWhat are public & private keys? allow you to make routing decisions and so on on IP packets. | UFW is a simplified firewall mechanism that is implemented on top of iptables. UFW is not as flexible but is easier to configure for common scenarios. |

 ### Ques : What are public & private keys?

When we use ssh-keygen command a public and private key is generated.

- A public key that is copied to the SSH server. Once an SSH server receives a public key from a user and considers the key trustworthy, the server marks the key as authorized in its authorized_keys file. Such keys are called authorized keys. Now the user with private key for this corresponding public key can connect to the server.
- A private key that remains only with the user. The possession of this key is proof of the user's identity. Only a user in possession of a private key that corresponds to the public key at the server will be able to authenticate successfully. The private keys need to be stored and handled carefully, and no copies of the private key should be distributed. The private keys used for user authentication are called identity keys.

 ### Ques : How ssh works?

The SSH protocol is based on the client-server model. Therefore, an SSH client must initiate an SSH session with an SSH server. The steps involved in creating an SSH session go like this:

- Client contacts server to initiate a connection.
- The server responds by sending the client a public cryptography key.
- The server negotiates parameters and opens a secure channel for the client.
- The user, through their client, logs into the server.

 ### Ques : Difference between HTTP & HTTPS.

HTTPS is HTTP with encryption. The only difference between the two protocols is that HTTPS uses TLS (SSL) to encrypt normal HTTP requests and responses. As a result, HTTPS is far more secure than HTTP. A website that uses HTTP has `http://` in its URL, while a website that uses HTTPS has `https://`.

 ### Ques : What is SSL?

SSL certificates are what enable websites to move from HTTP to HTTPS, which is more secure. An SSL certificate is a data file hosted in a website's origin server. SSL certificates make SSL/TLS encryption possible, and they contain the website's public key and the website's identity, along with related information. Devices attempting to communicate with the origin server will reference this file to obtain the public key and verify the server's identity. The private key is kept secret and secure.

###  Ques : Difference between apt update & apt upgrade.

| apt update                                                   | apt upgrade                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `apt update` is used to update the apt cache with the updated list of packages and its dependencies | `apt upgrade` is used to upgrade all the applications installed using apt package manager. |

 ### Ques : What are repositories in Linux?

Repositories in Linux is a storage location which consists large number of packages. For Ubuntu there are four main repositories:

- Main
- Universe
- Restricted
- Multiverse

 What does the number represent after the file permissions?

It dentoes the number of files in the directory. If its is a file, The number shows 1.

### Ques :  What does the number represent after the file permissions?

the number after the file permission respresent the memory block used by the file.

### Ques : Difference between apt and apt-get?

apt consists some of the most widely used features from apt-get and apt-cache leaving aside seldom used features. So with apt, we get all the necessary tools in one place. The main aim of apt is to provide an efficient way of handling package. It has fewer but sufficient command options but in a more organized way. On top of that, it enables a few options by default that is actually helpful for the end users.

### Ques : How can I give access to someone to my AWS instance?

i can give access to my anyone to my AWS instance by adding its public key to my authorised_key and then he can be known_host so he can easily get access to AWS instance.

### Ques : What are daemon Processes?

A daemon is basically processes running in background.

### Ques : What .d represent after a file?

"d" stands for directory and such a directory is a collection of configuration files which are often fragments that are included in the main configuration file. The point is to compartmentalize configuration concerns to increase maintainability.

### Ques : What happens when a pem file gets deleted?

if a pem is deleted then we are not able to access to instance but we can recover lost pem file with the availables options like creating new instance(helper instance).

### Ques : What information is stored in the /etc/host file?

The host file stores the hostname and ip address.This file is an ASCII text file. It contains **IP addresses separated by a space and then a domain name**. Each address gets its own line.

### Ques : What is SCP & what does this command do?

The SCP command or **secure copy allows secure transferring of files in between the local host and the remote host** or between two remote hosts. 

```bash
scp  /path/file_name ubuntu@ip destination
```

### Ques : How port forwarding works? 

**Port forwarding** is a technique that is used to allow external devices access to computers services on private networks. Local port forwarding is the most common type of port forwarding. It is used to let a user connect from the local computer to another server, i.e. forward data securely from another client application running on the same computer as a (SSH) client

### Ques : How can we connect without IP to AWS instance?

we can connect AWS instance without public IP addresses  **via their private IPv4 addresses** using  your own SSH client

### Ques :  What is an ssh agent?

ssh-agent is a key manager for SSH that keeps track of user's identity keys and their passphrases.

### Ques :  Create a unit file for any application.

To create unit file we must to be in /etc/systemd./system.

> [Unit]
> Description=mynginx- server start
>
> [Service]
> type=forking
> PIDFile=/run/nginx.pid
> WorkingDirectory=/usr/sbin/
> ExecStart=/usr/sbin/nginx
> ExecReload=/usr/sbin/nginx -s reload
> ExecStop=/bin/kill -s QUIT $MAINPID
> PrivateTmp=true
>
> [Install]
> WantedBy=multi-user.target

### Ques :  What is RHEL?

RHEL stands for **Red Hat Enterprise Linux** .It offers **flexibility of open source code and the innovation of open source communities**, along with certifications from hundreds of public cloud and service providers.

