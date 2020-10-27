---
description: just a small reminder that women can destroy your life
---

# GTA III

PS1 had GTA and GTA2, Xbox PS2 and PC had GTA 3 VC SA, PSP had LCS and VCS, and even the DS had CW. What a disapointment it was to see that the PSVita has no GTA games in its library. Even though they released all the GTA \(except VCS\) on mobile. Fortunately, thanks to a huge effort of the re3 modding group, they managed to decompile the game and thus making it possible to port it to multiple platforms. And that also include the PSVita thanks to a co effort from Rinnegatamante and TheFloW \(whenever there's GTA on vita you see him\).

## What do I need?

* A PSVita ofc
* The GTA III vpk and data files zip. Available [here](https://vitadb.rinnegatamante.it/#/info/589)
* A copy of GTA III. You can find one [here](https://store.steampowered.com/agecheck/app/12100/) or [here](https://www.rockstargames.com/fr/games/grandtheftauto3)
* The [batch script](https://github.com/AGraber/re3-nx/releases/download/23092020/convert_gta3_audio.zip) for the sounds credit : AGraber
* 50MB free in the memorycard for Textures Generations. \(The game will create a txd.img after you start it and it's 46MB\)

## The audio

By default you have compressed audio files, using those wav files like that will result in no audio in game and terrible performance because it will ask for the cpu to decode it. So we will do that ourselves.  


1. Open your GTA III folder
2. Go inside the audio folder
3. Drop the two files from the zip you have downloaded. 
4. Launch the bat file \(may need to open in with admin privilege.\)
5. It will create an audio folder containing audio files, this is the folder that we will use. 
6. Copy sfx.raw and sfx.SDT and all the MP3 files to the audio folder created.
7. Once it's done, we will swap the original audio folder with this one. Just move the audio folder created somewhere, delete the original audio folder, and put back in the GTA III folder the audio folder created \(Check that the folder contains 197 files to be sure\)

## Installing GTA III on your PSVita

You're nearly there, Send the vpk to your vita, and create a gta3 folder inside your data folder \(ux0:data/gta3\)

Put the game content inside the gta3 folder. Then open the data zip, and extract the content of the zip in the gta3 folder \(erase the files when asked\). 

Before you launch the game, make sure you don't have txd.img and txd.dir inside the models folder. You may already have those files if you used re3 before \(like the linux build\)

Install gta3.vpk and you can find a lovely bubble there. Start it, and let the fun begins !  
  
Note : In case you haven't read the psx post 



 We **strongly** suggest to set these specific settings to get the best experience in the Options menu:  


* **Frame Limiter: Off** \(Will allow the make to go over the 30 FPS original game lock\) 
* **Trails: Off** \(Trails effect is slightly off right now so produced quite undesiderable graphics effects\)
* **PostFX: Off** \(This will disable the blueish color washing filter original game has. In my opinion, with Trails disabled, this filter looks pretty bad so better to disable it\)
* **Screen Format: Auto** \(This will make the game be properly unstretched for Vita screen resolution\)



## Using HD models

So you played enough? You want to have those shiny models from the xbox version? You want to see fingers instead of plasticine? Well it's possible. Keep in mind that using those models will have a little impact on performance. Like an average of 27 fps instead of 30 fps, and in heavy locations it can go down to 20 fps instead of 22-23fps. But hey, are you more a graphic fan or performance fan?

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

Download the skin [there](https://cdn.discordapp.com/attachments/768443721447768096/769278769449533450/playa5_xbox.bmp) and put it inside the skin folder. Then you will have to chose it in the skin menu in game.

Xbox cars model : 

1. Download this[ archive](http://gta.rockstarvision.com/xbox_vehicles_iii.7z)
2. Extract the files
3. Put the vehicules xbox .img and .dir inside models folder
4. Put the wheels.dff inside models/Generic folder
5. Erase the current misc.txd inside the models folder with the one provided by the zip
6. open gta3.dat with a notepad and add the following line at the bottom

```text
CDIMAGE MODELS\VEHICLES_XBOX.IMG
```

Once it's done, remember to delete the txd.dir and txd.img from the models folder \(DONT PUT BACK THE ONE FROM THE ZIP\)

And that's it, you should now have better looking models in game \(just like the screenshots from vitadb\). Profit!

Note : With those, there is actually a little problem unsolved for now. When you will take the dodo and try to fly on the main runaway it will severly glitch and freeze. Just avoide that runaway and use the other one to take off



