Add Console Games to Hursty/Wolfanoz's Arcade Only RetroPie Image for Arcade1UP
=========

This guide covers how to add console games -- Genesis (aka Megadrive), SNES, NES, and TurboGrafx 16 -- to the very popular [Hursty/Wolfanoz Arcade Only RetroPie Image for Arcade1UP](https://www.arcadepunks.com/32gb-arcade-only-arcade1up-or-54-ratio-wolfanoz-hursty-collaboration/), and have the additions match the Hursty theme.

![GenesisSystem](https://raw.githubusercontent.com/patch-e/retropie-hursty-improvements/master/console-games/assets/genesis-system.png)  
![Genesis](https://i.imgur.com/oHoVtVR.jpg)  

![NESSystem](https://raw.githubusercontent.com/patch-e/retropie-hursty-improvements/master/console-games/assets/nes-system.png)  
![NES](https://i.imgur.com/Xfh9VTw.jpg)  

![SNESSystem](https://raw.githubusercontent.com/patch-e/retropie-hursty-improvements/master/console-games/assets/snes-system.png)  
![SNES](https://i.imgur.com/F4RPKOi.jpg)  

![TurboGrafx16System](https://raw.githubusercontent.com/patch-e/retropie-hursty-improvements/master/console-games/assets/tg16-system.png)  
![TurboGrafx16](https://i.imgur.com/mpq4BYu.jpg)  

([album link](https://imgur.com/gallery/D7leyx0))  

The console folders in this repository contain image assets that I designed to fit in perfectly with the Hursty theme. Each console gets it's own matching marquee/tile image along with a background image that combines each console's controller.

The asset folder in this repository contain the vector logos of each console and the Photoshop PSD that I created for each console along with the background.

Guide assumes you have already uploaded ROMs to the pi user's RetroPie `roms` folder. Optional steps at the end cover ROM upload and scraping.

## Steps to follow to install console additions to the theme:

1. access pi user over ssh  
   * password (if still the default): `raspberry`  
   * `ssh pi@retropie`  

2. enable root account by updating PermitRootLogin line in sshd_config  
   * open sshd_config in nano  
   * `sudo nano /etc/ssh/sshd_config`  
   * line should look like this (no # comment in front) `PermitRootLogin yes`  
   * ctrl-x to save file  

3. set root password  
   * password: enter password of your choice  
   * `sudo passwd root`  

4. reboot to activate root account  
   * `sudo shutdown -r now`  

5. access root user over ssh  
   * password: password chosen earlier  
   * `ssh root@retropie`  

6. upload megadrive, nes, snes, and tg16 folders in this repository to pi  
   * copy the folders to `/etc/emulationstation/themes/hurstyuparcade_aspectratio54/`  

7. reboot to activate theme additions  
   * `sudo shutdown -r now`  

8. repeat steps 1-4 to disable root account  
   * in step 2 comment out PermitRootLogin  
   * line should look like this `# PermitRootLogin yes`  

## The remaining steps are optional if you need to upload console ROMs to your pi

9. obtain ROM files :)  

10. access pi user over ssh  
    * password (if still the default): `raspberry`  
    * `ssh pi@retropie`  

11. upload ROM files to megadrive, nes, snes, and tg16 folders on pi  
    * roms are stored here `/home/pi/RetroPie/roms`  
    * ex. `/home/pi/RetroPie/roms/nes`  

12. Follow [Stephen Selph's Scraper](https://github.com/RetroPie/RetroPie-Setup/wiki/Scraper#steven-selphs-scraper) guide to scrape thumbnails and descriptions of the megadrive, nes, snes, and tg16 systems.