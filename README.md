#  Killer E2400 in Linux (Ubuntu, Debian) 

## alx driver
The Killer E2400 has been confirmed to work fully by modifying and loading the alx driver in Ubuntu 14.04 and 15.04. These changes have been upstreamed and should work natively in future Linux kernels.

This is a DKMS version of the alx driver using the 4.4 kernel source code 

## Instructions: How to install

###Make sure your complier enviroment is ready.

sudo apt-get source linux-image-$(uname-r) 

###Run the following commads: 

sudo apt-get install git dkms build-essential linux-headers-generic
git clone https://github.com/teocci/alx.git
sudo dkms add ./alx
sudo dkms build alx/2.0
sudo dkms install alx/2.0

###Reboot

This driver has been tested on the 3.13.0-24 kernel and it works along with 4.2 kernel.
