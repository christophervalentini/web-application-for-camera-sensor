# web-application-for-camera-sensor
Christopher Valentini 191007
UniTN - Embedded Systems course - Web Application for Camera Sensor project


HOW TO INSTALL AND SET UP THE APPLICATION:
(Tested on Ubuntu 19.04 - 19.10)

-Check your python3 version. Be sure it is >=3.6:

python3 -V

-Install dependencies:

sudo apt-get install python3 ffmpeg streamer python3-pip libatlas-base-dev libqtgui4 python3-pyqt4 libqt4-test python3-opencv  
sudo apt-get install libjasper-dev 

(on some architectures libjasper-dev may not be present and/or not necessary) 

-Install pip modules on python=>3.7:

pip3 install schedule numpy flask flask_cors opencv-python

(WARNING: opencv-python module python=>3.6 for ARM CPU causes some errors using the Raspberry! Do not install it) 

-If you want to use Python3.6 (instead of =>3.7):

	sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev

	wget https://www.python.org/ftp/python/3.6.8/Python-3.6.8.tgz
	tar -xvf Python-3.6.8.tar.xz 
	cd Python-3.6.8
	./configure (Here you may want to set a different path)
	make
	sudo make install

	-You should uprgrade pip.
	sudo python3.6 -m pip install --upgrade pip 

	-If pip is not installed, you have to reconfigure Python3.6.8 and set the path to /usr/local/bin 

	-Install pip modules on python3.6:
	python3.6 -m pip install schedule flask flask_cors numpy opencv-python

	-Edit start_webapp_offline.sh
	'python3 main.py' to 'python3.6 main.py'


-Make the script executable and run the application:

chmod +x start_webapp_offline.sh

./start_webapp_offline.sh

-OR, if you use the Raspberry:

chmod +x start_webapp_offline_raspberry.sh

./start_webapp_offline_raspberry.sh

-If you get the error 'no module named cv2', be sure to have the package 'python3-opencv' installed, or the 'opencv-python' pip module. On the Raspberry do not use pip module opencv-python


Note: python3.6.8 lib works fine, with a newer version bugs may occour.


For contacts:
Christopher Valentini
c.valentini-1@studenti.unitn.it
christopher.valentini@gmail.com
