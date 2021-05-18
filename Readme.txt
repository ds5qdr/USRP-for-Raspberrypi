DVSwitch USRP Client for RaspberryPi

This Program is modified and compiled pyUC.py (DVSwitch Client USRP) by DS5QDR
https://github.com/DVSwitch/USRP_Client


Newest Version
2021.05.18 V2.30


Manual (Comartable with Windows version)
https://ds5qdr-dv.tistory.com/214


Hardware 
- RaspberryPi 3B 4B
- USB Sound Card
- 3.5 inch LCD 이상 (GPIO, HDMI any)
- Compartable with DVPi system


How to setup

----------------------------------------------------------------------
for DVPi system

echo Download USRP for Raspberrypi files from github
sudo git clone https://github.com/ds5qdr/USRP-for-Raspberrypi USRP
cd USRP

echo Setting 
sudo chown pi:pi *
sudo chmod +x USRP dmr_status
sudo mv /home/pi/dvpi/dvpi /home/pi/dvpi/dvpi_go
sudo mv dvpi dvpi.jpg /home/pi/dvpi/
sudo mv dvpi.desktop USRP.desktop /home/pi/desktop

echo reboot
sudo reboot 

------------------------------------------------------------------------
for Debian or Rasbian system

echo Download USRP for Raspberrypi files from github
sudo git clone https://github.com/ds5qdr/USRP-for-Raspberrypi USRP
cd USRP

echo Setting 
sudo chown pi:pi *
sudo chmod +x USRP dmr_status
sudo mv USRP.desktop /home/pi/desktop

echo reboot
sudo reboot


------------------------------------------------------------------------
and then You can find USRP icon on Desktop windows of Rasbian.
click USRP !

or open terminal and then
cd USRP
./USRP




for more information go to below site!
https://ds5qdr-dv.tistory.com/218


공개 이력
2020.12.16 V0.95 : pyUC.py 를 수정하고 실행파일로 만들어 첫 공개
2021.01.04 V1.00 : USRP Client Released for Windows
2021.01.21 V1.65 : 세로모드에서 가로모드로 해상도 및 Layout 변경 (800x480)
2021.02.01 V1.80 : DMR TG Status 기능 추가
2021.02.15 V1.90 : 기존 DMR, DSTAR 에 NXDN, P@%, YSF Mode 추가 지원
2021.03.24 V2.00 : DVSwitch Web 버젼 hUC All Mode 지원 (STFU, Intercom, ASL Mode)
2021.04.30 V2.20 : Remote DVS Restart, TG/REF List 자동 다운로드 및 DVS 설정 기능 추가 (진행중) 


DS5QDR Lee, Heonmin
