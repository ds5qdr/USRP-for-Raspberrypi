# USRP_for_Raspberrypi
- Version : V3.11
- Updated Date : 2021.10.31
- Programmed by DS5QDR Lee, Hoenmin

# History
- 2021.10.31 V3.10 : fixed QRZ image download error and simplified
- 2021.10.09 V3.00 : [MACRO] command added to control DVSwitch Server
- 2021.09.23 V2.95 : [SERVER] section of usrp.ini has changed since V2.95 at as below
- 2021.03.24 V2.00 : support DVSwitch hUC (STFU, Intercom, ASL Mode) 
- 2021.01.04 V1.00 : USRP Client Released for Windows
- 2020.12.16 V0.95 : pyUC.py compiled to pyUC.exe

# How to install 
- wget http://xlx841ysf.duckdns.org/usrp/usrp_install
- sudo chmod +x usrp_install
- ./usrp_install 

# How to update
- click 'Control' tab of USRP, click 'Upgrade USRP' button!

# Warning
- Don't install Pulseaudio, it makes R2D2 when Rx/Tx transmit
- Install only Pyaudio, https://github.com/DVSwitch/USRP_Client
- to remove Pulseaudio 
- sudo apt purge pulseaudio

# Other Audio setting
- sudo nano /usr/share/alsa/alsa.conf
- defaults.ctl.card 0 ---> 2
- defaults.pcm.card 0 ---> 2

# Modify /boot/config.txt to match Video resolution
- sudo nano /boot/config.txt
- add 5 lines at the end of config.txt
- hdmi_group=2
- hdmi_mode=1
- hdmi_mode=87
- hdmi_cvt 800 480 60 6 0 0 0
- hdmi_drive=2

# how to edit usrp.ini
- see : http://dvswitch.org/DVSwitch_install.pdf
- Appendix B: pyUC (python USRP Client)
![image](https://user-images.githubusercontent.com/64110724/134375327-b36d3c95-b887-4ac5-82a7-c5c620e5acfe.png)


# [SERVER] section of usrp.ini has changed since V2.95 at as below
- [SERVER] #server_name   : callsign :dmrid   : repeaterid  DDNS or IP address : USRP_rx/txport : usrp2dvs_port
- DVS_00 = DefaultDVS     : DS5QDR  : 4500495 : 450049599 : ds5qdr-dvs.iptime.org : 59595 : 61301 : 
- DVS_01 = DVS_SAMPLE     : DS5QDR  : 4500495 : 450049599 : ds5qdr-dvs.iptime.org : 59595 : 61301 : 
- DVS_NM = 4500495 : DS5QDR : Heonmin : Lee : Gimhae : KyungSang Nam-Do : Korea Republic of :
- If you use the version before V2.95, Please reconfigure the usrp.ini file.

# for more information
- click here, https://ds5qdr-dv.tistory.com/224

# DS5QDR Lee, Heonmin
![image](https://user-images.githubusercontent.com/64110724/139769083-80591158-ab74-4c9b-894a-022539d05d08.png)
![image](https://user-images.githubusercontent.com/64110724/139767788-b128b603-d6a0-4282-9933-1aa0a8bc4c06.png)
![image](https://user-images.githubusercontent.com/64110724/139768191-90c9b12e-06d7-402c-ade0-124f866f540c.png)
![image](https://user-images.githubusercontent.com/64110724/139768448-920d5901-2600-4dba-8311-ebd70a48f25a.png)
![image](https://user-images.githubusercontent.com/64110724/139768977-3315f195-a05b-4229-be9a-9b06479808e8.png)

