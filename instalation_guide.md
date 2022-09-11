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
11. type mkdir droid
12. type cd droid
13. type sudo nano pi_droid.py
14. copy text for pi_droid.py (local) to the new file
15. press ^x to exit
16. press Y to save
17. type python pi_droid.py to run the file

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







