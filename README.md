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

그리고 기본설정/Rasberry Pi Configuration/Set Resolution 에서 해상도를 조절

마지막으로 재부팅해주면 적용된다
sudo reboot
