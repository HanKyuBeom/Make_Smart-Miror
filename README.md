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
