## Linux File System

File system is used to handle the data management of the storage.
## Linux vs Windows File System

 ![Screenshot 2022-08-18 at 1.01.29 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660764696945/t-3r0Cfjk.png align="left")

> - Linux File System has a hierarchical tree structure and uses Ext4, ZFS, JFS, btrfs etc.
> - It has only **1 root folder**.
> - Existence of swap partitions, you never run out of memory in Linux (like in windows).

   **Windows in comparison**

![windows-10-c-drive-full.webp](https://cdn.hashnode.com/res/hashnode/image/upload/v1660767987026/2m43s-ylgz.webp align="left")

> - Windows uses** FAT** (File Allocation Table) and **NTFS **(New Technology File system).
> - It has **multiple** root folders.

## Does Linux use NTFS?
NTFS file-storing system is standard on Windows machines, but Linux systems also use it to organize data. 

#  EVERYTHING in Linux is a FILE
Everything in the system is represented by a file descriptor,
Text documents, pictures etc,
Commands like pwd, ls etc,
Devices like printer, keyboard, USB,
even directories. 
Linux makes no difference between a file and a directory, since a directory is just a file containing names of other files.



![FY054uhUIAAnj6r.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1660769259509/R34FqgY_R.jpg align="left")

**Unlike Windows or other operating-systems, Here in Linux root(/) is the base and all other files are the children. Let’s discuss each of them in detail.**

### 1. /
Root
> -  In the Linux file system, everything comes under the root directory.
> - The root user's home directory is at /root.

### 2./home 
Contains home directories of all the non-root users.
> - Possible to have multiple user accounts on 1 computer.
> - Each user has its own space.
> - Each user can have own configurations.

 ### 3. /bin
 Binaries; executables for most essential user commands.
> - A binary file is a computer- readable format.
> - These are the commands which are available to all the users. Commands like cd, mv, nano etc are loading from here.
![Screenshot 2022-08-18 at 2.35.40 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660770348418/avNNbLfYb.png align="left")

### 4. /sbin 
System binaries; essential system binaries programs that admin would use.
> - There are some binary files which are hidden from normal users. 
> - These commands are available to root users. 
> - System binary executable commands such as ifconfig, fdisk can be accessed from here.
![Screenshot 2022-08-18 at 2.40.38 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660770643992/zwNU-eczZ.png align="left")

### 5. /lib
Library; essential shared libraries that executables from /bin or /sbin use.
> - Contains shared libraries which are often used by the '/bin' and '/sbin' directories.
> - It also contains kernel module.
> - These filenames are identable as ld* or lib*.so.*. For example, ld-linux.so.2 and libfuse.so.2.8.6.
![Screenshot 2022-08-18 at 2.44.58 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660770905737/RypkXh0xf.png align="left")

### 6. /usr
User; used for user home directories.
 
- ** /usr/local **
> - Programs that you install on the computer, third-party applications like docker, minikube, java etc.
> - Programs installed here will be available for all users on the computer.
> - Inside /usr/local: App installation will be split again into different folders.
>  ![Screenshot 2022-08-18 at 3.00.09 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660771814153/X_PFzbEhU.png align="left")


## Do you what's the history behind two  /bin files?
Because of **storage limitations**, it was split to root binary folders and user binary folders.

###  7. /opt
Optional; third-party program you install.

**So what's the difference between /usr/local and /opt?**.
> - Third-party apps whose components aren't split between bin and lib files use /opt files.
      > - Programs, which split its components uses /usr/local.
> - **/opt** is used for those program which do not split it components. Example: IDE, Web Browser.

### 8. /etc
Et cetera 
 > - Contains system-wide configuration files.
> -  Here you’ll find configuration files of most of the applications and user configuration files.
> -  For example, Linux stores the password of each user in this directory.

### 9. /tmp
Temporary
 > - This is a volatile directory.
 > - Applications use this directory to store the temporary files until the system reboots.
 > - If any application crashes you can recover the files here.

### 10. /boot
Booting; contains files required for booting.
> - Files that are required to boot into your systems such as grub and EFI.
> - Messing with these files can make your system not boot.

### 11. /dev
Devices; location of device files like webcam, keyboard, hard drive etc.
> - Apps and Drivers will access this, NOT the user.
> - Files that the system needs to interact with the device.

### 12. /var
Variable; contains files to which the system writes data during the course of its operation.
> - /var/log : Contains log files
> - /var/cache: Contains cached data from application programs

###  13. /media
> - Contains subdirectories, where removable media devices inserted into the computer are mounted.
> - E.g. when you insert a CD. A directory will automatically be created and you can access the contents of the CD inside the directory.

###  14. /mnt
> - Temporary mount points.
> - Historically, system administrators mounted temporary file systems here.


## Hidden Files
> - Hidden files are primarily used to help prevent important data from being accidentally deleted.
> - Automatically generated by programs or OS.
> - File name starts with a dot.
![Screenshot 2022-08-18 at 3.46.11 AM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660774577722/Gl1NaR1W1.png align="left")
















