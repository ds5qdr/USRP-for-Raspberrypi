## USRP-for-RaspberryPi with Logbook
- Version : V3.951
- Updated Date : 2023.04.21
- Programmed by DS5QDR Lee, Hoenmin
- USRP1132 <--- USRP for debian 11 bullseye 32bit


## History
- 2023-04-21 V3.951: fixed bugs and updated
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
```
wget http://usrp.duckdns.org/usrp_install
sudo chmod +x usrp_install
./usrp_install 
```


## Download file USRP or USRP64 manually
```
cd /home/pi/USRP
sudo wget -O /home/pi/USRP/USRP usrp.duckdns.org/USRP32 <--- debian 10 Buster or 11 Bullseye 32bit
sudo wget -O /home/pi/USRP/USRP usrp.duckdns.org/USRP64 <--- Debian 11 Bullseye 64bit
sudo chmod +x /home/pi/USRP/USRP
./USRP
```

## Warning
```
# if R2D2 accurs, modify daemon.conf
sudo nano /etc/pulse/daemon.conf
default-fragments = 5
default-fragment-size-msec = 2
```

## Other Audio setting (install script change below settings automatically)
```
sudo nano /usr/share/alsa/alsa.conf
defaults.ctl.card 0 ---> 2 or 1
defaults.pcm.card 0 ---> 2 or 1 
( aplay -l command show your USB sound card no. whether 0, 1 or 2 )
```

## Modify /boot/config.txt to match Video resolution
```
sudo nano /boot/config.txt
# add 5 lines at the end of config.txt
hdmi_group=2
hdmi_mode=1
hdmi_mode=87
hdmi_cvt 800 480 60 6 0 0 0
hdmi_drive=2
```

## how to edit usrp.ini
- see : http://dvswitch.org/DVSwitch_install.pdf
- Appendix B: pyUC (python USRP Client)
![image](https://user-images.githubusercontent.com/64110724/134375327-b36d3c95-b887-4ac5-82a7-c5c620e5acfe.png)

## How to add PTT
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/bb172318-ce33-43b2-b251-6730a74e615e)

## for more information
- click here, https://ds5qdr-dv.tistory.com/417

# DS5QDR Lee, Heonmin
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c46f33cc-56b9-4e8a-8d44-eb578ba4ad7e)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c20ed2d1-bf83-45f0-bd3c-8250586a9a7c)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/7fe55ff9-7098-48e6-8d0a-4dbe4f2c1a6f)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/d08105b5-2972-4e05-9ea5-6f5887f45cc4)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c0c34564-8274-45aa-a1e9-4d27c695422c)

