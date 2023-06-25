# Table of Contents


## Hardware
***
- 1 - Raspberry Pi zero W
- 1 - 16 GB SD Card
- 2 - LM2596 Buck Converter
- 1 - L298N Stepper motor Driver
- 1 - Relay


## Setup Instructions
***
### setup raspberry
1.  Download Raspberry Pi Imager
2.  Choose operating system - Raspberry PI OS Lite (legacy) (Recommended)
3.  Select Storage 
4.  Click Write (Configure setting before hand if you wish)
5.  When completed remove disk and insert in to Raspberry Pi Zero
6.  Boot up device
7.  conntect to pi using SSH
8.  Login to device
9.  Run sudo apt update
10. Run sudo apt upgrade 

### install webcam using motion
1.  type sudo apt-get install motion
2.  connect usb webcam
3.  type lsusb
4.  Type sudo nano /etc/motion/motion.conf
5.  set daemon to on
6.  press ctrl+w
7.  type framerate
8.  set to 100
9.  press ctrl+w
10. type live stream
11. set stream_localhost to off
12. arrow up to webcontrol_localhost set it to off
13. press ctrl+w
14. type quality
15. set to 100
16. press ctrl+w
17. type post_caption
18. set to 5      
19. press ^x to exit
20. press Y to save
21. Type sudo service motion restart 
22. type sudo motion
23. got to web browers ipaddress:8081


### install node.js
1. go to https://nodejs.org/dist/
2. copy link https://nodejs.org/dist/latest-v11.x/node-v11.15.0-linux-armv6l.tar.gz (may be newer version)
3. SSH into raspberry Pi
4. run curl -o node-v11.15.0-linux-armv6l.tar.gz https://nodejs.org/dist/latest-v11.x/node-v11.15.0-linux-armv6l.tar.gz
5. tar -xzf node-v11.15.0-linux-armv6l.tar.gz
6. cd node-v11.15.0-linux-armv6l
7. sudo cp -R * /usr/local/
8. node -v
9. npm -v 
10. sudo apt-get install git
11. Create webserver dir in home (local) 
12. sudo chmod ugo+rwx webserver (changes permision on folder)
13. cd webserver
14. run npm init
15. npm install onoff
16. npm install socket.io -save
17. sudo apt install libcap2-bin
18. sudo setcap cap_net_bind_service=+ep /usr/local/bin/node
19. getcap -r /usr/ (to check permisions)


### Updating files 
1. cd /usr/local/webserver/gpio/
2. sudo git pull origin main
3. node webserver.js






