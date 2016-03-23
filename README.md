# Gamestarter

![gamestarter-logo](https://raw.githubusercontent.com/bite-your-idols/gamestarter-openelec/master/assets/gamestarter-logo.jpg)


### About
I'm trying ot make a very easy installation for Retroarch and other games or emulators for Raspberry Pi's OpenELEC.
It is based on originally addon created by Mezo in OpenELEC official forums and edited by other forum users.


This is still a work in progress project.



### Installation instructions:

Connect to your Raspberry Pi via [ssh](http://wiki.openelec.tv/index.php/OpenELEC_FAQ#How_do_i_use_SSH.3F) and type:

```
wget --no-check-certificate -O /storage/install-gamestarter.sh https://raw.githubusercontent.com/bite-your-idols/gamestarter-openelec/master/install-gamestarter.sh
```

Then:
```
sh /storage/install-gamestarter.sh
```

relax and wait 5 minutes...

After that, you should reboot your system and copy your roms, bios and saves to /storage/emulators/ folder via ftp or [samba](http://wiki.openelec.tv/index.php/Accessing_Samba_Shares).




### Post-installation setup:

After installation is completed and reboot, firts thing you have to do is transfer some roms and requiered bios. 
Then, there are two ways of launching RetroArch. The easiest one is using the addon that is located under Program Addons called Gamestarter: Retroarch. 

The first time RetroArch is launched I recommend to Update everything (Settings menu> Online Updater). The you can create your own playlists, start games, change cores, user dynamic wallpapers, boxarts, update cores,... just like in [Lakka](http://www.lakka.tv/) distro!!

Instead os using this addon you can [remap your remote](http://kodi.wiki/view/HOW-TO:Modify_keymaps) and assign to a key the following action:
```
XBMC.System.Exec("/storage/emulators/scripts/gamestarter.sh retroarch")
```

The other way to launch RetroArch games, and the only one to launch both amiga roms and GameMaker Pi ports, is using AdvancedLauncher, located also under Program Addons.

There it is a default/example launchers/games list I created. You can edit list



WIP...



### ToDo:
- Include sample roms/games
- Create uninstall and update scripts for libretro cores and RetroArch.
- WIP...



### Bugs, issues, errors...:
- No sound in emualtors:
```
mount -o remount,rw /flash
nano /flash/config.txt 
```
Add this lines:
```
hdmi_force_edid_audio=1
dtparam=audio=on
```
Exit saving and reboot.


WIP...




### Credits:

- Original RetroArch addon by Mezo:
 http://openelec.tv/forum/128-addons/72972-retroarch-addon-arm-rpi

- Retroarch:
http://www.libretro.com/

- UAE4ARM:
https://www.raspberrypi.org/forums/viewtopic.php?t=110488

- GameMaker:
http://yoyogames.com/pi

- AdvancedLauncher:
https://github.com/edwtjo/advanced-launcher

- Hacklib:
http://forum.kodi.tv/showthread.php?pid=1481392#pid1481392

- System thumbs by tronkyfran:
https://github.com/HerbFargus/es-theme-tronkyfran


Enjoy!