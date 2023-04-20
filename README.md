## USRP-for-RaspberryPi with Logbook
- Version : V3.90
- Updated Date : 2023.01.30
- Programmed by DS5QDR Lee, Hoenmin


## History
- 2023.01.30 V3.90 : Simplify USRP Client UI and added Analog Tranceiver Interface
- 2022.11.07 V3.70 : upgraded some fucntions and fixed bugs
- 2022.04.01 V3.60 : added DTMF fucntion ( option : SA818 module interface )
- 2022.04.07 V3.50 : USRP is for 32bit, USRP64 is for 64bit OS
- 2022.01.01 V3.40 : added LOG BOOK, click Callsign at main screen -> Callsign_logbook.json
- 2021.12.16 V3.30 : added 5 option choice and fixed bugs
- 2021.11.29 V3.20 : upgrade some fucntions and fix bugs
- 2021.10.31 V3.10 : fixed QRZ image download error and simplified
- 2021.10.09 V3.00 : [MACRO] command added to control DVSwitch Server
- 2021.09.23 V2.95 : [SERVER] section of usrp.ini has changed since V2.95 at as below
- 2021.03.24 V2.00 : support DVSwitch hUC (STFU, Intercom, ASL Mode) 
- 2021.01.04 V1.00 : USRP Client Released for Windows
- 2020.12.16 V0.95 : pyUC.py compiled to pyUC.exe


## Option 1] Download DVSwitch + USRP All-in-one IMG file (micro SD 16G Image)
- click link to https://ds5qdr-dv.tistory.com/417
- see readme.txt
- login ID : pi   
- password : usrp    
- VNC PW   : usrp


## Option 2] How to install manually on Rasberrypi OS (Debian 10 or 11)
- wget http://usrp.duckdns.org/usrp_install
- sudo chmod +x usrp_install
- ./usrp_install 


## Download file USRP or USRP64 manually
- stop USRP
- cd /home/pi/USRP
- sudo wget -O /home/pi/USRP/USRP usrp.duckdns.org/USRP32 <--- debian 10 Buster or 11 Bullseye 32bit
- sudo wget -O /home/pi/USRP/USRP usrp.duckdns.org/USRP64 <--- Debian 11 Bullseye 64bit
- sudo chmod +x /home/pi/USRP/USRP
- ./USRP


## Warning
- if R2D2 accurs, modify daemon.conf
- sudo nano /etc/pulse/daemon.conf
- default-fragments = 5
- default-fragment-size-msec = 2


## Other Audio setting (install script change below settings automatically)
- sudo nano /usr/share/alsa/alsa.conf
- defaults.ctl.card 0 ---> 2 or 1
- defaults.pcm.card 0 ---> 2 or 1 
- ( aplay -l command show your USB sound card no. whether 0, 1 or 2 )


## Modify /boot/config.txt to match Video resolution
- sudo nano /boot/config.txt
- add 5 lines at the end of config.txt
- hdmi_group=2
- hdmi_mode=1
- hdmi_mode=87
- hdmi_cvt 800 480 60 6 0 0 0
- hdmi_drive=2


## how to edit usrp.ini
- see : http://dvswitch.org/DVSwitch_install.pdf
- Appendix B: pyUC (python USRP Client)
![image](https://user-images.githubusercontent.com/64110724/134375327-b36d3c95-b887-4ac5-82a7-c5c620e5acfe.png)

## How to add PTT
![image](https://user-images.githubusercontent.com/64110724/152883240-493c3906-e9c3-4d5e-874d-d906b0391a36.png)

## for more information
- click here, https://ds5qdr-dv.tistory.com/417

# DS5QDR Lee, Heonmin
![image](https://user-images.githubusercontent.com/64110724/139769603-f42fc40e-5d56-472e-b3df-74af970e5c04.png)
![image](https://user-images.githubusercontent.com/64110724/139767788-b128b603-d6a0-4282-9933-1aa0a8bc4c06.png)
![image](https://user-images.githubusercontent.com/64110724/139768191-90c9b12e-06d7-402c-ade0-124f866f540c.png)
![image](https://user-images.githubusercontent.com/64110724/139768448-920d5901-2600-4dba-8311-ebd70a48f25a.png)
![image](https://user-images.githubusercontent.com/64110724/139768977-3315f195-a05b-4229-be9a-9b06479808e8.png)

