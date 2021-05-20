# how-to-fix-busybox-initramfs-error-on-ubuntu

step 1 run exit command

then the result look like

(initramfs) exit
/dev/sda1 contains a file system with errors, check forced.
Inode 4326476 extent tree (at level 1) could be narrower, IGNORED.
/dev/sda1: Inode 4326843 extent tree (at level 1) could be narrower, IGNORED.
/dev/sda1: Inode 4327012 extent tree (at level 1) could be narrower, IGNORED.
/dev/sda1: Inode 4329004 extent tree (at level 1) could be narrower, IGNORED.
/dev/sda1: Inodes that were part of a corrupted orphan linked list found.

/dev/sda1: UNEXPECTED INCONSISTENCY; RUN fsck MANUALLY.
        (i.e., without -a or -p options) 
fsck exited with status code 4. 
The root filesystem on /dev/sda1 requires a manual fsck. 

BusyBox v1.30.1 (Ubuntu 1:1.30.1-4ubuntu6.1) built-in shell (ash)
Enter 'help' for a list of built-in commands.



here we can see that that is the mount point


step 2   run this command fsck /dev/sda1 -y

step 3 reboot system
