# android-server-setup
Implementing server in android phone

## System configuration
* Android 6
* Moto G

## Setup process:
* Install userland app in android phone.
* **ONLY version 2.8.3** works you need to get it(apk) outside playstore.
* Install unbuntu and do following:
   *  Basic system update:
      *  `sudo apt-get update && sudo apt-get upgrade`
   *  Install ssh:
      *  Run these commands:
      ```
      sudo apt-get install net-tool
      sudo apt-get install iptables
      sudo update-alternatives --list iptables
      sudo update-alternatives --set iptables /usr/sbin/iptables-legacy
      sudo apt-get install openssh-server 
      ```
      *  Get the IP of android system:  `hostname -I`
      * Login into ssh: `ssh <user_name>@<ip of system> -p 2022
    


