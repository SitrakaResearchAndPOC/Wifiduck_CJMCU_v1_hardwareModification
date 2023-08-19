# Wifiduck_CJMCU_v1_hardwareModification
# Wifi ducky Description problem
* Hardware descripition
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard1.png" width="750px" align="center">
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard2.jpeg" width="750px" align="center">
* Problems of continuity   
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard3.png" width="750px" align="center">
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard4.png" width="750px" align="center">

# Installing driver of USB (could be CP21x, FT23X, CH340G, PL23X)
(In my case, it's [CP21x](https://drive.google.com/file/d/18dX5ws61_A4EaHKuIYNDSMMeMPuJHZG5/view?usp=drive_link))
* [CH34xG](https://www.wch-ic.com/downloads/CH341SER_ZIP.html)
* [FTDI and FT232RL](https://ftdichip.com/drivers/)
* [CP210x](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)

# Finding port of CJMCU
* plug CJMCU
* search : "devices manager" and click it
* click "Ports (COM and LTP)"
* remind the number of port come noted as COMX
* click on COMx and click "all parameters" memories the baudrates note as Y 
* Close all

# Downloading firmeware of esp8266_wifi_duck
* [esp12e_wifiduck.cjmcu3212.bin](https://drive.google.com/file/d/1TyeB8ZIUXi7tQGnCArDZb7wSMjctTNOa/view?usp=drive_link)
  
# Installation ESP8266Flasher
* Download [esp8266Flasher](https://drive.google.com/file/d/1YC0DqRsgMTjVpCc77wQt9xKFKphjFWGM/view?usp=drive_link)
* Launch ESP8266Flasher.exe

# Flashing esp8266_wifi_duck
* Download Arduino and televersing this code [step1](https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_old/blob/main/step1.ino)  (select following port and type of board before televersing) 
* Connect The two pins as :
  <img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_old/blob/main/cjmcu2.jpeg" width="750px" align="center">
  <img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_old/blob/main/cjmcu3.jpeg" width="350px" align="center"></img>

* Run esp8266 flasher named as  : ESP8266Flasher.exe
* In operation, Change port com as COMx
* In config, change with the firmeware esp12e_wifiduck.cjmcu3212
* In Advanced, change bauderate as Y at the first step
* After successfull flashing, don't connect the two pins as in the first step
* Download this code [arduino_ducky_cjmcu3212](https://raw.githubusercontent.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/main/atmega_duck.rar)
* Televersing the code atmega_duck.ino (select following port and type of board before televersing)

# Hardware solutions (connection SDA and SCL) 
* solution hardware
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard5.jpeg" width="750px" align="center">
  
* solution software  
<img src="https://github.com/SitrakaResearchAndPOC/Wifiduck_CJMCU_v1_hardwareModification/blob/main/cjmcu_hard6.jpeg" width="750px" align="center">

 
# Using wifiduck
* Reuplug the wifiduck
* Finding wifi network name <i>wifiduk</i> and password <i>quackquack</i> or <i>wifiduck</i>
* On broswer, enter: http://192.168.4.1
* Testing duckyscript as you need

# Ducky Script example
```
DEFAULTDELAY 200  
LOCALE FR  
GUI r  
STRING CMD  
ENTER  
```

# Documentations
* https://github.com/SpacehuhnTech/WiFiDuck/issues/124
* https://github.com/TomFang1/WiFiDuck_CJMCU_3212/tree/master
