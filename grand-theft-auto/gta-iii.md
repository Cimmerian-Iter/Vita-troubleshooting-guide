---
description: just a small reminder that women can destroy your life
---

# GTA III

PS1 had GTA and GTA2, Xbox PS2 and PC had GTA 3 VC SA, PSP had LCS and VCS, and even the DS had CW. What a disappointment it was to see that the PSVita has no GTA games in its library. Even though they released all the GTA \(except VCS\) on mobile. Fortunately, thanks to a huge effort of the re3 modding group, they managed to decompile the game and thus making it possible to port it to multiple platforms. And that also includes the PSVita thanks to a co effort from Rinnegatamante and TheFloW \(whenever there's GTA on vita you see him\).

## What do I need?

* A PSVita ofc
* The GTA III vpk and data files zip. Available [here](https://vitadb.rinnegatamante.it/#/info/589)
* A copy of GTA III. You can find one [here](https://store.steampowered.com/agecheck/app/12100/) or [here](https://www.rockstargames.com/fr/games/grandtheftauto3)
* The [batch script](https://github.com/AGraber/re3-nx/releases/download/23092020/convert_gta3_audio.zip) for the sounds credit : AGraber
* 2.3GB +50MB free in the memorycard for Textures Generations. \(The game will create a txd.img after you start it and it's 46MB\)
* [FdFix](https://github.com/TheOfficialFloW/FdFix) plugin by TheFloW \(Not needed if you have already repatch\)

If you have a problem, check the common error section first before asking for help.

**Note: If you want to update gta3 to 1.1 you will have to redownload the gamesfile.zip from vitadb and extract its content in the gta3 folder. Then remove txd.img and txd.dir again from the models folder.**

## The audio

By default you have compressed audio files, using those wav files like that will result in no audio in game and terrible performance because it will ask for the cpu to decode it. So we will do that ourselves.  


1. Open your GTA III folder
2. Go inside the audio folder
3. Drop the two files from the zip you have downloaded. 
4. Launch the bat file. It will create an audio folder containing audio files, this is the folder that we will use. 
5. Copy sfx.raw and sfx.SDT and all the MP3 files to the audio folder created. \(If the MP3 are already in the folder forget it\)
6. Once it's done, we will swap the original audio folder with this one. Just move the audio folder created somewhere, delete the original audio folder, and put back in the GTA III folder the audio folder created \(Check that the folder contains 197 files to be sure\)

## Installing GTA III on your PSVita

First you need to install the FdFix plugin, it will solve the problem of apps crashing when you put your vita into sleep mode, and other errors that may arise from the sleeping mode.  
NOTE : If you already have the repatch plugin, there is no need for you to install this. Skip the plugin installation part

Once you have downloaded the plugin, just install it like any plugins \(If you don't know how to install a plugin, check the [plugin section ](https://samilops2.gitbook.io/vita-troubleshooting-guide/plugins-related-problem/error-when-using-autoplugin)of this guide.\)

add this line to the config.txt \(the one you use, either inside ux0:tai or ur0:tai\)

```text
*KERNEL
ux0:tai/fd_fix.skprx
```

Once the plugin is installed and you rebooted your vita, you are nearly there. Send the vpk to your vita, and create a gta3 folder inside your data folder \(ux0:data/gta3\)

Put the game content inside the gta3 folder. Then open the data zip, and extract the content of the zip in the gta3 folder \(erase the files when asked\). 

Before you launch the game, make sure you don't have txd.img and txd.dir inside the models folder. You may already have those files if you used re3 before \(like the linux build\)

Install gta3.vpk and you can find a lovely bubble there. Start it, and let the fun begins !  
  
Note : In case you haven't read the psx post 

We **strongly** suggest to set these specific settings to get the best experience in the Options menu:

* **Frame Limiter: On** \(You don't want some broken physics\)
* **Trails: Off** \(Trails effect is slightly off right now so produced quite undesirable graphics effects\)
* **Colour Filter: Off** \(This will disable the blueish color washing filter original game has. In my opinion, with Trails disabled, this filter looks pretty bad so better to disable it\)
* **Wide Screen: Auto** \(This will make the game be properly unstretched for Vita screen resolution\)
* **Frame Sync: Off** \(May cause some minor glitches in exchange of some slight framerate boost\)
* **Draw Distance** \(Lowering this gives a consistent framerate boost, suggested to drop it to lowest\)

Also in controls settings, set controls to classic

![If you ever want to set correctly the controls.](../.gitbook/assets/image%20%2811%29.png)

## Common Errors

* Q : I launched GTA3 but it crash in the splash loading screen.  A : You missed the part where you should had copied back the MP3 and sfx files to the generated audio folder. If you have bought the rockstar games version, there are some report of it not working. Let me check what's wrong with that version and I'll update that
* Q : The script won't launch A : If the game is located inside C:\programmes\(x86\) you need to move the gta3 folder elsewhere like in Documents and then run the script
* Q : In game works but radio doesn't play. My audio folder is 300MB not 2GB A : Some pirated version of the game create blank .wav for the radio so the overall weight of the gta3 game is lowered. Better buy a legit version

## Using HD models

So you've played enough? You want to have those shiny models from the xbox version? You want to see fingers instead of plasticine? Well it's possible. Keep in mind that using those models will have little impact on performance. Like an average of 27 fps instead of 30 fps, and in heavy locations it can go down to 20 fps instead of 22-23fps. But hey, are you more a graphic fan or performance fan?

Let's first use the xbox peds files : 

1. Download the following [zip](http://gta.rockstarvision.com/xbox_peds_cdimage.zip)
2. Extract the contents to the models folder
3. open default.dat inside the data folder with notepad
4. add this line at the bottom \(it doesn't actually matter where exactly you put the line\)

```text
CDIMAGE MODELS\XBOX_PEDS.IMG
```

Onto the next part, the player model. If you don't want claude to look like that, you need to use the xbox model of claude.

![pain](../.gitbook/assets/image%20%2810%29.png)

Download the skin [there](https://cdn.discordapp.com/attachments/768443721447768096/769278769449533450/playa5_xbox.bmp) and put it inside the skin folder. Then you will have to choose it in the skin menu in game.

Xbox cars model : 

1. Download this[ archive](http://gta.rockstarvision.com/xbox_vehicles_iii.7z)
2. Extract the files
3. Put the [vehicles xbox .img](https://drive.google.com/file/d/14Lh5Lo_NQkoWWilXRpQOd_WQplMf3IdX/view?usp=sharing) and .dir inside models folder \(use this .img instead of the one from the zip, this is an updated version made to fix the polygon explosion. You can still use the vehiclesxbox.dir file from the zip.\)
4. Put the wheels.dff inside models/Generic folder
5. Erase the current misc.txd inside the models folder with the one provided by the zip
6. open gta3.dat with a notepad and add the following line at the bottom

```text
CDIMAGE MODELS\VEHICLES_XBOX.IMG
```

Once it's done, remember to delete the txd.dir and txd.img from the models folder \(DONT PUT BACK THE ONE FROM THE ZIP\)  
  
Last part, road textures. You can see more information about it [here](http://gta.rockstarvision.com/workshop/hires_txds/)

Download the generic\_iii\_pc.txd, rename it to generic.txd and replace the original generic.txd with that one.

And that's it, you should now have better looking models in game \(just like the screenshots from vitadb\). Profit!





