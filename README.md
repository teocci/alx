# alx
I made this DKMS version of the ALX driver using the 4.4 kernel source code 

## Instructions: How to install

sudo apt-get install git dkms build-essential linux-headers-generic
git clone https://github.com/jeremyb31/alx.git
sudo dkms add ./alx
sudo dkms build alx/2.0
sudo dkms install alx/2.0

Reboot

I have tested this in the old 3.13.0-24 kernel and it works along with 4.2 which correctly states that this is exactly the same as the module present in the kernel
