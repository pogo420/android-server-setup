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
      * Login into ssh: `ssh <user_name>@< ip of system > -p 2022
    
   *  Install git:
   *  `sudo apt install git`
    
   *  In the end do this again:
      *  `sudo apt-get update && sudo apt-get upgrade`

## Hardware status:
* Secondary memory check `df -h /`
* Primary memory check `free -h -w`

## Important info:
* Ports below 1000 are reserved by android.
* File transfer:
  `scp -P <ssh port>  -r dist/* <server_user>@<server_ip>:/location/to/keep/file`

* Deploy Angular application:
  * Go to the level having index.html
  * Run this command: `python3 -m http.server 8080`
  
