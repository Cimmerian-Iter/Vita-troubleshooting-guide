---
description: Because we need bubbles in our lives.
---

# Making Custom Bubbles

Playing Super Mario 64 on the Vita is no longer a meme (well we could always use DaedalusX64 in Adrenaline) and you want to celebrate it by making a nice and shiny bubble you will pin on the first page? But you're confused as to how to do that? Then you're in the right place!

## What do I need?

* A Vita (ofc)
* A Windows PC (well, Linux and MacOS users can always try to use wine, Catalina users will have to use bootcamp)
* A rom of your game
* DaedalusX64 installed and working (with the data files)
* [The builder files](https://github.com/Rinnegatamante/DaedalusX64-vitaGL/releases/download/Nightly/builder.zip)

## Ok, got it, which file should I open?

The file you need to launch is the build.bat. You will have a nice CMD window asking you 3 things (don't worry, it's not some hacker stuff nor complicated command line process like h-encore)

* Name of the .vpk: Either simple like supermario64 or something fancy like peachgotcapturedagainpart4 if you like.
* The name of the rom. You will need to enter the path of the rom. Standard path for roms is ux0:data/DaedalusX64/Roms so, for example, you will need to input `ux0:data/DaedalusX64/Roms/sm64.n64`. But if you want a custom path it should still work. For example: `ux0:roms/sm64.n64`
* The title ID: This part is up to you, it must be 9 letters in uppercase and can contain numbers. You can't use the same title ID for 2 bubbles, each one is unique. `DAEDALUS3` will work, `SuPeRmArIo` won't because it's not 9 characters and not full uppercase. Avoid using any title IDs found [here](https://vitadb.rinnegatamante.it/#/titleids).

Once it's done it will generate a .vpk file that you can install on your Vita. That's all you have to do to have a custom bubble!

## That's nice and all, but I don't want another Daedalus bubble, I want a Super Mario themed bubble

Yeah OK, it's all grey and it's not fun, we got it. You can customize the background and the icon app if you want. You must respect the following rules:

* Background picture is a .png file and has dimensions of 840x500. The file must be named: bg.png
* Icon picture is a .png file and has dimensions of 128x128. The file must be named: icon0.png
* Startup button icon is a .png file and has dimensions of 280x158. The file must be named: startup.png

Nearly there, we still need to do a last conversion. The Vita only allows 8bit .png's. In order to respect this limitation we will use pngquant for the conversion. You can grab pngquant from [here](https://pngquant.org) (Download the Windows binary)\
Once you have it, follow these instructions :

1. Put the .png files in a folder, and extract pngquant into the same folder
2. Open a CMD window and cd to the directory which contain the png and pngquant. If you don't know how to use the cd command, search \[duckduckgo]\(https:// duckduckgo.com/) to learn how.
3. Do the following command for each .png: pngquant nameofthepng.png
4. After the conversion is done, you will have a nameofthepng-fs8.png file, rename them to their correct name and that's all!

Once it's done, you can put all these .png files in the asset folder and run build.bat again, it will generate a .vpk with your Super Mario themed bubble.

![Oh, a Mario head](<../.gitbook/assets/image (16).png>)

![No Vita? No problem, vita3K exists](<../.gitbook/assets/image (3) (1).png>)

And that's it, you have a nice Super Mario themed bubble. I chose Super Mario 64 as an example but you can do the same thing with any game you want. Enjoy!
