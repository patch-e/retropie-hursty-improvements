Add Console Games to Hursty/Wolfanoz's Arcade Only RetroPie Image for Arcade1UP
=========

This guide covers how to add console games -- NES, SNES, Genesis (aka Megadrive), and TurboGrafx 16 -- to the very popular [Hursty/Wolfanoz Arcade Only RetroPie Image for Arcade1UP](https://www.arcadepunks.com/32gb-arcade-only-arcade1up-or-54-ratio-wolfanoz-hursty-collaboration/), and have the additions match the Hursty theme.

* ![Genesis](https://i.imgur.com/oHoVtVR.jpg)  
* ![NES](https://i.imgur.com/Xfh9VTw.jpg | width=100)  
* ![SNES](https://i.imgur.com/F4RPKOi.jpg | width=100)  
* ![TurboGrafx16](https://i.imgur.com/mpq4BYu.jpg | width=100)  
* ([album link](https://imgur.com/gallery/D7leyx0))  

The console folders in this repository contain image assets that I designed to fit in perfectly with the Hursty theme. Each console gets it's own matching marquee/tile image along with a background image that combines each console's controller.

The asset folder in this repository contain the vector logos of each console and the Photoshop PSD that I created for each console along with the background.

Steps to follow to install console additions to the theme:

1. access pi user over ssh  
   password (default): raspberry  
   `ssh pi@retropie`

2. enable root account  
   change “PermitRootLogin yes”  
   ctrl-x save  
   `sudo nano /etc/ssh/sshd_config`  

3. set root password  
   password: (enter password of your choice)  
   `sudo passwd root`  

4. reboot  
   `sudo shutdown -r now`  

5. access root user over ssh  
   password: (password chosen earlier)  
   `ssh root@retropie`  

6. upload nes, snes, megadrive, and tg16 folders to pi  
   copy the folders to `/etc/emulationstation/themes/hurstyuparcade_aspectratio54/`  

7. exit root ssh session  
   `exit`  

8. to be continued...  
