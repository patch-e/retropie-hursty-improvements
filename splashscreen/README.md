RetroPie Custom Splashscreens for Arcade1UP
=========

## Steps to follow to upload and apply new splashscreens

1. access pi user over ssh  
   * password (if still the default): `raspberry`  
   * `ssh pi@retropie`  

2. upload videos to pi
   * copy the files to `/home/pi/RetroPie/splashscreens`

3. choose which splashscreen to use
   * open splashscreen.list in nano  
   * `sudo nano /etc/splashscreen.list`  
   * modify path to mp4, ex. `/home/pi/RetroPie/arcade1up-retropie.mov`  
   * ctrl-x to save file  

4. reboot to activate added setting  
   * `sudo shutdown -r now`  

5. enjoy new splashscreen
