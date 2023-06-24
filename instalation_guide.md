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
2.  Choose operating system - Raspberry PI OS Desktop (Recommended)
3.  Select Storage 
4.  Click Write (Configure setting before hand if you wish)
5.  When completed remove disk and insert in to Raspberry Pi Zero
6.  Boot up device
7.  conntect to pi using SSH
8.  Login to device
9.  Run sudo apt update
10. Run sudo apt upgrade
11. 

### install webcam using motion
1.  type sudo apt-get install motion
2.  connect usb webcam
3.  type lsusb
4.  Type sudo nano /etc/motion/motion.conf
5.  set daemon to on
6.  press ctrl+w
7.  type framerate
8.  set to 1500
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
2. copy link https://nodejs.org/dist/v9.7.1/node-v9.7.1-linux-armv6l.tar.gz (may be newer version)
3. SSH into raspberry Pi
4. run curl -o node-v9.7.1-linux-armv6l.tar.gz https://nodejs.org/dist/v9.7.1/node-v9.7.1-linux-armv6l.tar.gz (same link as above)
5. tar -xzf node-v9.7.1-linux-armv6l.tar.gz
6. sudo cp -r node-v9.7.1-linux-armv6l/* /usr/local/
7. node -v
8. npm -v 
9. sudo apt-get install git
10. Create webserver dir in home (local) 
11. run npm init
12. npm install onoff
13. npm install socket.io -save
14. sudo apt install libcap2-bin
15. sudo setcap cap_net_bind_service=+ep /usr/local/bin/node
16. getcap -r /usr/ (to check permisions)


### Updating files 
1. go to /home/pi
2. sudo git pull origin main
3. cd back
4. sudo cp -R /home/pi/* /usr/local/webserver/gpio/
5. cd /usr/local/webserver/gpio/
6. node webserver.js






