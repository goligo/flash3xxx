= Scripts for flashing Enterasys/Extreme Networks 3xxx devices with OpenWrt =

These scripts do automate the tasks to flash 3xxx access points. They are useful in case a lot of devices need to be flashed to reduce manual work. 

Currently OpenWrt does only support 3710 and 3825 models. The scripts strictly follow the steps as described in 

https://github.com/openwrt/openwrt/commit/16b01fb1b9c99513c318109bef96a1a3545c57a0

and

https://github.com/openwrt/openwrt/commit/7e614820a89208c4e91a3a5f9de07a5402accdaa

To be able to run the scripts, the following preconditions must be met:
* A linux machine, other unixish devices may work, but have not been tested
* Cisco console cable connected to the AP
* Network cable connected to the AP (for AP3825 to LAN 2 port)
* IP-addresses 192.168.200.200 and 192.168.1.100 assigned to the connected network interface
* TFTP-Server installed and running, with root directory writable by the user (e.g. tftpd-hpa) 
* expect, cu, wget and ssh installed

Warning: These scripts do not do backups of the existing firmware partitions, you can not easily move back to the original firmware. 

To flash devices, please adapt the configuration variables in the scripts, like the tty-device or the tftp root folder. Then you can just start it and follow the instructions.
