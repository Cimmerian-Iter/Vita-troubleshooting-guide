---
description: just a small reminder that women can destroy your life
---

# GTA III

PS1 had GTA and GTA2, Xbox PS2 and PC had GTA 3 VC SA, PSP had LCS and VCS, and even the DS had CW. What a disapointment it was to see that the PSVita have no GTA in its library. Even though they released all the GTA \(exept VCS\) on mobile. Fortunately, thanks to a huge effort of the re3 modding group, they managed to decompile the game and thus making it possible to port it to multiple platform. And that include the PSVita too thanks to a co effort from Rinnegatamante and Thefl0w \(whenever there's GTA on vita you see him\).

## What do I need?

* A PSVita ofc
* The GTA III [vpk](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
* A copy of GTA III. You can find one [here](https://store.steampowered.com/agecheck/app/12100/) or [here](https://www.rockstargames.com/fr/games/grandtheftauto3)
* The data file zip that you can find in vitadb
* The [batch script](https://github.com/AGraber/re3-nx/releases/download/23092020/convert_gta3_audio.zip) for the sounds 
* libshacccg.suprx \(First test if it works, like see if in Daedalus-X64, the modern render is greyed out\)

## The audio

By default you have compressed audio files, using those wav files like that will result in no audio in game and terrible performance because it will ask for the cpu to decode it. So we will do that ourselves.  


1. Open your GTA III folder
2. Go inside the audio folder
3. Drop the two files from the zip you have downloaded. 
4. Launch the bat file \(may need to open in with admin privilege.\)
5. It will create a audio folder containing audio files, this is the folder that we will use. 
6. Copy sfx and sfx.SDT and all the MP3 files to the audio folder created.
7. Once it's done, just move the audio folder created somewhere, delete the original audio folder, and put back in the GTA III folder the audio folder created \(Check that the folder contains 197 files to be sure\)

## Installing GTA III on your PSVita

You're nearly there, Send the vpk to your vita, and create a gta3 folder inside your data folder \(ux0:data/gta3\)

Put the game content inside the gta3 folder. Then open the data zip, and extract the content of the zip in the gta3 folder \(erase the files when asked\). And you are done. Install gta3.vpk and you can find a lovely bubble there.

