DVSwitch USRP Client for RaspberryPi

This Program is modified and compiled pyUC.py (DVSwitch Client USRP) by DS5QDR
https://github.com/DVSwitch/USRP_Client


최신버젼
2021.04.01 V2.05 : 일부 오류 개선


사용설명서 (Windows 버젼과 동일)
https://ds5qdr-dv.tistory.com/214


추천 Hardware 사양
- RaspberryPi 3B 이상
- USB Sound Card
- 3.5 Inch LCD 이상 (GPIO, HDMI 모두 지원)
- DVPi 시스템과 100% 호환


설치 방법 (아래 명령어 한줄씩 실행하세요)
echo Download USRP for Raspberrypi files from github
sudo git clone https://github.com/ds5qdr/USRP-for-Raspberrypi USRP
cd USRP

echo Setting 
sudo chmod +x USRP dmr_status
sudo mv /home/pi/dvpi/dvpi /home/pi/dvpi/dvpi_go
sudo mv dvpi dvpi.jpg /home/pi/dvpi/
sudo mv dvpi.desktop USRP.desktop /home/pi/desktop

echo reboot
sudo reboot 


사용방법 아래 링크 참고하세요
https://ds5qdr-dv.tistory.com/218


공개 이력
2020.12.16 V0.95 : pyUC.py 를 수정하고 실행파일로 만들어 첫 공개
2021.01.04 V1.00 : USRP Client Released for Windows
2021.01.21 V1.65 : 세로모드에서 가로모드로 해상도 및 Layout 변경 (800x480)
2021.02.01 V1.80 : DMR TG Status 기능 추가
2021.02.15 V1.90 : 기존 DMR, DSTAR 에 NXDN, P@%, YSF Mode 추가 지원
2021.03.24 V2.00 : DVSwitch Web 버젼 hUC All Mode 지원 (STFU, Intercom, ASL Mode)


DS5QDR Lee, Heonmin
