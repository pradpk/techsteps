## File Structure & File Systems

- Linux follows FHS (Filesystem Hierarchy Standard) in 
which all files are directories appear under the 
root / directory (even if they are stored in different
 physical or virtual devices).
- We have to understand that not all Linux distributions follow this.

### Linux Directories

- /bin - Binaries containing basic command programs like ls,
cat, chown which you run on linux OS.
- /sbin - System binaries that are used by System Administrators
and it contains programs for commands for which normal user will not 
access to.
- /boot - contains files Linux used to boot
- /dev - contains device files. /dev/sda contains disk devices.
/dev/mapper contains logical volumes. Applications and drivers 
will use this directory.
- /etc - contains system-wide configurations.
- /home - you can store your personal files since each user 
has their own home folder.
- /lib, /lib32, /lib64 - libraries containing files that 
are used by binaries and applications.
- /media, /mnt - contain mounted drives such as floppy 
disk, usb stick, hard drive, network drive. It is similar 
to A: and B: drive in Windows when it used floppy to boot.
- /opt - normally contains manually installed softwares and
applications.
- /proc - contains files about system process. Kernel will 
create the files within this directory for all the processes
which appears when we look for process data. Example to get
cpuinfo, we can get it from cat /proc/cpuinfo.
- /root - root user's home folder. Need root permission
to access it.
- /run - mostly contains runtime info which will be created  
during initial bootload (it may be used differently on 
different dist os).
- /srv - contains service specific files
- /sys - system folder files to interact with kernel.
- /tmp - temporary files
- /usr - contains user application files. /usr contains subset copy
of the dir structure of linux (has /bin, /sbin, /lib etc).
- /var - variable directory contains files that can grow.
Example log files.

### File Systems

Reference: https://www.youtube.com/watch?v=_h30HBYxtws

- File systems divide the storage space into virtual 
compartments known as clusters and maintain index where 
individual files are located.
- FAT, NTFS, exFAT are mostly used in Windows file systems.
- FAT (File Allocation Table) - Different variants such 
as FAT12, FAT16 & FAT32 - each has an increasing number of clusters and
max file size (FAT32 - 4GB, FAT16 - 2GB) and volume size. FAT32 is popular
as it is compatible across OS.
- NTFS (New Technology File System) - File size limit of 16EB (1 EB = 1 million TB).
Supports file permissions and encryption. Windows must be installed on NTFS drive.
- exFAT - Extended File Allocation Table - File system optimized for 
high capacity USB drives and memory cards. Max file size is 16EB. Default 
file system for SD cards.
- ext2, ext3 & ext4 (extended file system) - ext4 is the latest version 
of file system and has become Linux default file system. Max size of ext4 is 
16TB and volumes up to 1 EB.
- HFS, HFS+ (Hierarchical File System - MacOS) - was default file system on MacOS. 
Not supported by Windows or Linux.
- APFS (Apple File System) - Optimized for SSD.
- ZFS (Zed File System) 

#### Usage
- Windows - NTFS
- Linux - ext4
- macOS - HFS+, APFS
- USB drives & Memory Cards - FAT32 (under 32GB), exFAT (greater than 32 GB) 
- SSD or external hard drive - exFAT
 


 

