# USRP_for_Raspberrypi
- Version : V2.95
- Updated Date : 2021.09.06
- Programmed by DS5QDR Lee, Hoenmin

# How to install 
- wget http://ds5qdr-dvs.iptime.org/usrp/usrp_install
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


# usrp2dvs 
- If you want to use full fucntion you have to install usrp2dvs program at your DVSwitch server
- to install, click 'Server' tab
- enter DVSwitch IP address, login ID and PW and then click 'install'
- After install, you must open portforwad UDP Port at your internet router.
- UDP Port is Analog_Bridge.ini [USRP] section tx/rxPort + 1  ex) tx/rxPort = 50000 UDP Port is 50001
-----------------------------------------------------------------------------------------------------
- Manual installation at DVSwitch Server
- connect to your DVSwitch
- sudo git clone https://github.com/ds5qdr/USRP2DVS /opt/usrp2dvs
- sudo chmod +x /opt/usrp2dvs/usrp2dvs
- sudo chmod +x /opt/usrp2dvs/rc.local
- sudo mv /opt/usrp2dvs/rc.local /etc


# for more information
- click here, https://ds5qdr-dv.tistory.com/224

# DS5QDR Lee, Heonmin

![image](https://user-images.githubusercontent.com/64110724/134379674-5fa1f607-64ad-40fb-9909-cfedb49b3076.png)
![image](https://user-images.githubusercontent.com/64110724/129439515-706fb468-88c0-4ae9-8df7-2b9cf832451a.png)
![image](https://user-images.githubusercontent.com/64110724/129439571-aaa1a5e0-25fe-4f3e-bad2-e7906a455fa6.png)

