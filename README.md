# Make_Smart-Miror

pi@raspberrypi ~ $ sudo apt-get update


pi@raspberrypi ~ $ sudo apt-get upgrade

git설치
pi@raspberrypi ~ $ sudo apt-get install git-core

https://github.com/HackerHouseYT/Smart-Mirror 를 설치

git에서 다운로드하기
git clone git@github.com:HackerHouseYT/Smart-Mirror.git

Smart-Mirror파일로 이동
cd Smart-Mirror

pip설치
sudo pip install -r requirements.txt
sudo apt-get install python-imaging-tk

nano로 필요한 부분 수정
sudo nano smartmirroor.py

Smart-Mirror실행
python smartmirror.py

화면회전하기
sudo nano /boot/config.txt

맨 마지막 줄에 추가하기 0 = 0도, 1 = 90도, 2 = 180도, 3 = 270도
display_rotate=1

스크린 보호기 화면 잠금 풀기

>절전 모드 관련
cd /etc/lightdm/lightdm.conf

sudo nano lightdm.conf

80번째 줄에 [SeatDefaults]에서
(#xserver-command=X)를
(#xserver-command=X -s 0 dpms)
로 저장합니다.

>스크린 세이버(화면보호기)
cd /etc/X11/xinit/xinitrc

sudo nano xinitrc

8번째쯤 줄에  /etc/X11/Xsession이 보입니다.
밑으로 3줄을 추가합니다.

xset s off
xset -dpms
xset s noblank

저장하고 리부팅합니다.

기본설정/Rasberry Pi Configuration/Set Resolution 에서 해상도를 조절

마지막으로 재부팅해주면 적용된다
sudo reboot
