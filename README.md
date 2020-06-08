# roger-skyline-1
**Initiation to system and network administration**

## VM part
VM creation


### Specifics
+ Hypervisor: Virtual Machine
+ Linux OS: Ubuntu 18.04 (64-bit)
+ Image: ubuntu-18.04.2-live-server-amd64.iso
+ Size of harddisk: 8.00GB (fixed size)
+ Partition set manually to 4.2 GB


### Installation
+ Initiate your virtual machine.
+ Choose the ubuntu iso as your disk.
+ Set your name, your server name, username and password.
+ Mark the Install OpenSSH Server.
+ Don’t install any other server environments.

+ Update and upgrade your Ubuntu OS system on root:

`sudo -i`

+ Run:

`apt-get update -y && apt-get upgrade -y`

+ To list all block devices, run:

 `lsblk`

+ List Partitions Under Linux
`sudo fdisk -l`

+ List packages scheduled for the update
You can view the list of packages that have a newer version ready to be upgraded. 
For this, run the following command in Terminal:
`apt list --upgradeable`

### Dependencies
+ To install all of the dependencies for the Firewall, webserver and mail run on the terminal as root:

`apt-get install sudo vim ufw portsentry fail2ban apache2 mailutils -y`


## Network and Security Part

### Configure Sudo

1. **Use sudo, with the non-root user specified during install, to be able to perform operation requiring special rights.**
+ Login as root:

`sudo -i` 

+ **Type `visudo` on the terminal.**
At # User privilege specification add:

` youruser   ALL=(ALL:ALL) NOPASSWD:ALL`

+ **Check if user is added to the sudoers file:**

`cat /etc/sudoers`

### Setup a static IP

1. **We don’t want you to use the DHCP service of your machine. You’ve got to configure it to have a static IP and a Netmask in \30**
+ 



