## USRP-for-RaspberryPi with Logbook
- Version : V4.00
- Updated Date : 2025.04.08
- Programmed by DS5QDR Hoenmin Lee in Gimhae, Korea
- USRP1132 <--- USRP for debian 11 bullseye 32bit


## History
- 2025-04-08 V4.00 : Final Version. 
- 2024.03.17 V3.98 : It's probably the final version
- 2023.04.21 V3.95 : fixed bugs and updated
- 2023.01.30 V3.90 : Simplify USRP Client UI
- 2022.11.07 V3.70 : upgraded some fucntions and fixed bugs
- 2022.01.01 V3.40 : added LOG BOOK, click callsign at main screen -> ADD/DEL/ALL -> save to usrp_logbook.json
- 2021.12.16 V3.30 : added 5 option choice and fixed bugs
- 2021.11.29 V3.20 : one click auto upgrade USRP.exe for Windows version
- 2021.10.31 V3.10 : fixed QRZ image download error and simplified
- 2021.10.09 V3.00 : [MACRO] command added to control DVSwitch Server
- 2021.09.23 V2.95 : [SERVER] section of usrp.ini has changed since V2.95 at as below
- 2021.03.24 V2.00 : support DVSwitch hUC (STFU, Intercom, ASL Mode) 
- 2021.01.04 V1.00 : USRP Client Released for Windows
- 2020.12.16 V0.95 : pyUC.py compiled to pyUC.exe


## Option 1] Download DVSwitch + USRP All-in-one IMG file (micro SD 16G Image)
- click link to https://ds5qdr-dv.tistory.com/544
- see readme.txt
- login ID : pi   
- password : usrp    
- VNC PW   : usrp


## Option 2] How to install manually on Rasberrypi OS (Debian 11 Bullseye)
```
wget http://dvdown.duckdns.org/program/usrp/usrp_install
sudo chmod +x usrp_install
./usrp_install 
```


## Download file USRP for Debian 11 Bullseye 32bit manually
```
cd ~
mkdir USRP
cd USRP
sudo wget -O ~/USRP/USRP dvdown.duckdns.org/program/usrp//USRP1132 <--- debian 11 Bullseye 32bit
sudo chmod +x /home/pi/USRP/USRP
./USRP
```

## Other Audio setting (install script change below settings automatically)
- see below
- https://ds5qdr-dv.tistory.com/544


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
- click here, https://ds5qdr-dv.tistory.com/544

# DS5QDR Lee, Heonmin
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c46f33cc-56b9-4e8a-8d44-eb578ba4ad7e)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c20ed2d1-bf83-45f0-bd3c-8250586a9a7c)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/7fe55ff9-7098-48e6-8d0a-4dbe4f2c1a6f)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/d08105b5-2972-4e05-9ea5-6f5887f45cc4)
![image](https://github.com/ds5qdr/USRP-for-Raspberrypi/assets/64110724/c0c34564-8274-45aa-a1e9-4d27c695422c)

