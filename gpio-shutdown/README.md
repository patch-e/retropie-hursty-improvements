GPIO Shutdown for Arcade1UP Power Switch
=========

## Steps to follow to use the stock power switch for turning your pi on/off

1. Plug power switch connector to raspberry pi's GPIO 5th and 6th pins  
   * The black wire should be on the 5th pin (inside of pi board)  
   * The red wire should be on the 6th pin (outside of pi board)  

2. access pi user over ssh  
   * password (if still the default): `raspberry`  
   * `ssh pi@retropie`  

3. add dtoverlay to config.txt  
   * open config.txt in nano  
   * `sudo nano /boot/config.txt`  
   * add line to the bottom of the config with this value `dtoverlay=gpio-shutdown`  
   * ctrl-x to save file  

4. reboot to activate added setting  
   * `sudo shutdown -r now`  

5. enjoy usable power switch
