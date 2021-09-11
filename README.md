# USRP_for_Raspberrypi
- Version : V2.94
- Updated Date : 2021.09.06
- Programmed by DS5QDR Lee, Hoenmin

# How to install 
- wget http://ds5qdr-dvs.iptime.org/usrp/usrp_install
- sudo chmod +x usrp_install
- ./usrp_install 

# How to update
- click 'Control' tab of USRP, click 'Upgrade USRP' button!

# Warning
- Don't install Pulseaudio, it makes R2D2 at Rx/Tx
- Install only Pyaudio, https://github.com/DVSwitch/USRP_Client
- to remove Pulseaudio 
- sudo apt purge pulseaudio

# Other Audio setting
- sudo nano /usr/share/alsa/alsa.conf
- defaults.ctl.card 0 ---> 2
- defaults.pcm.card 0 ---> 2

# modify /boot/config.txt to match Video resolution
- sudo nano /boot/config.txt
- add 5 lines as below
-     hdmi_group=2
-     hdmi_mode=1
-     hdmi_mode=87
-     hdmi_cvt 800 480 60 6 0 0 0
-     hdmi_drive=2

# usrp2dvs 
- If you want to use full fucntion you have to install usrp2dvs program at your DVSwitch server
- to install, click 'Server' tab
- enter DVSwitch IP address, login ID and PW and then click 'install'
- After install, you must open portforwad UDP Port at your internet router.
- UDP Port is Analog_Bridge.ini [USRP] section tx/rxPort + 1  ex) tx/rxPort = 50000 UDP Port is 50001

# for more information
- click here, https://ds5qdr-dv.tistory.com/224

# DS5QDR Lee, Heonmin

![image](https://user-images.githubusercontent.com/64110724/129439417-da88633c-1f49-4744-ad14-89e6ed44eb68.png)
![image](https://user-images.githubusercontent.com/64110724/129439515-706fb468-88c0-4ae9-8df7-2b9cf832451a.png)
![image](https://user-images.githubusercontent.com/64110724/129439571-aaa1a5e0-25fe-4f3e-bad2-e7906a455fa6.png)

