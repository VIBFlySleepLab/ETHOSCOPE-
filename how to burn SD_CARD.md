Create your SD card using an image file   .img
=======================

SD card model = SAMSUNG EVO 32 GB
file used for image.  20160427_ethoscope.img  **using usb flash to copy this file to desktop**

in terminal : 
[node@node ~]$ `su` # as  super user 
password `node`    **current password**
[root@node node]# `fdisk -l`
find the name of sd card: in this case it is **sda**  **very careful with dd. You want to write on the write drive!**
[root@node node]# `dd if=/home/node/Desktop/20160427_ethoscope.img of=/dev/sda bs=64K`.
		``dd if=/home/node/Desktop/20180530_ethoscope.img of=/dev/sda bs=64K``
enter wait
finsh



 
Change the id of the card as explained 

Then you want so change the ID of the machine in the card, so rewrite:
* `/etc/machine-id`. This is a hexadecimal unique name for the machine. You can put some random string *prefixed with a number*. For instance `001ae2f5cee1`...
* `/etc/machine-name`. This is the human friendly name of the machine. For instance ETHOSCOPE_001.
* `/etc/hostname`. This is the name of the machine on the network. For example you could put e001.



Testing
================

The simple way to test your machine is to *plug a screen* add boot your new SD card.

