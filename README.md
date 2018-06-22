# IoT_Assignment2

1. Remove dhcpcd  
sudo systemctl disable dhcpcd.service  

2. Bind device name with MAC address  
edit /etc/udev/rules.d/10-network.rules  
* wlan0 - onboard, ad-hoc  
* wlan1 - dongle, connect AP  

3. Set mode for both wlan  
edit /etc/network/interfaces  

4. Set wifi for wlan1  
edit /etc/wpa_supplicant/wpa_supplicant.conf  

5. Install msquitto server on Gateway  
apt-get install mosquitto  
apt-get install mosquitto-clients  

6. Configure mosquitto as a bridge  
mosquitto -c /etc/mosquitto/conf.d/AWS_gateway.conf -v  

7. Install Bluepy on Pi  
sudo apt-get -y install bluez build-essential libglib2.0-dev libdbus-1-dev python-dev  
sudo pip install bluepy  

8. MAC address f SensorTag  
54:6C:0E:53:19:84 CC2650 SensorTag  

9. Run sensortagcollector_iot.py  
web - https://developer.ibm.com/recipes/tutorials/connecting-multiple-ti-sensortags-to-iot-platfom-using-a-raspberry-pi-gateway/  
download - https://ibm.box.com/shared/static/pwkgxejzk92ktjn53owm1ka6bom9o0oq.zip  

10. Install paho  
git clone https://github.com/eclipse/paho.mqtt.python.git  
cd paho.mqtt.python  
sudo python setup.py install  

11. Modify node-red  
