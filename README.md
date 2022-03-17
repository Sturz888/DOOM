# DOOM
Run DOOM on raspberry pi 0

Here is a link to the tutorial I followed https://pimylifeup.com/raspberry-pi-doom/

#### you will need : 
-Raspberry Pi
-Micro SD Card
-Power Supply
-Ethernet Cable or Wi-Fi
-HDMI Cable
-USB Keyboard
-Mouse

#### what to do
Before we begin we must ensure your pi is up to date

run ``` sudo apt update```
otherwise your pi may try to pull from a mirror that doesn't exist

when that is finished you can run
``` sudo apt install chcocolate-doom -y```
this installs the game but wait, we still have get the WAD file

To store these WAD file we must create a new folder,
go to your games folder within /usr
```mkdir /usr/games/Doom```

then change to that directory
```cd /usr/games/Doom```

we will now use the 'wget' command to pull the WAD file

```wget https://files.pimylifeup.com/doom/shareware_doom_iwad.zip```
now unzip these files with ```unzip shareware_doom_iwad.zip```
then remove the zip ```rm shareware_doom_iwad.zip```

you should have a file named DOOM.WAD in the Doom directory,
to make sure use command ```ls```

This should be ready to go but before we start we need to configure the mouse and keyboard (or gamepad)
use command ```chocolate-doom-setup``` and you can go through the options you wish to change.
you will have the option to save and run DOOM when you done

to start the game without configuring use ```chocolate-doom -iwad /usr/games/Doom```

If you do not want to type that command you can run the script file DOOM.sh which is included. You just need to create a script directory in root then put DOOM.sh in there

```cd~```
```sudo mkdir scripts```

Download the DOOM.sh then move it into the scripts directory.

#HAVE FUN

