# Preparations

## Getting a JabirOS session 

You need to be permitted to use a _JabirOS_ session, or you can test this piece of software on a _Debian Live Disc_ or any other Linux system. We suggest using this piece of software on a JabirOS session though. 

When you got your session and boot the _ISO_ image on a machine (real hardware or virtual machine), you need to login to the system. Login with the user `root` and password `toor`. 

## Partitioning the disk

This part, is a bit tricky. If you are about to install this on a VM, the hard disk is usually detected as `/dev/vda`. On a real machine or some of more _test_ hypervisors such as [Virtual Box](https://virtualbox.org) it can be `/dev/sda`. Using `lsblk` command on the session, you can see disks and partitions available. 

We assume your hard drive is `/dev/vda`. Now, you can use `cfdisk` to do the partitioning. We suggest at least 10 gigabytes of space for a clean JabirOS session installation, do partitioning like this: 

- at least 2 GB for _swap_ (if you have 1 or 2 gigabytes of RAM)
- at least 3 or 4 GB for _root_. 
- the rest for _/home_. 

## Partition end-points

assuming you made a 2 GB partition for swap, 3 GB for root and 5 GB for home in this order, you'll have: 

- `/dev/vda1` for swap
- `/dev/vda2` for root 
- `/dev/vda3` for home 

Now, you can go to the [installation](INSTALLATION_PROCESS.md) guide for doing the rest of the installation process. 