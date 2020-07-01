---
description: Because we need bubbles in our lives.
---

# Making Custom Bubbles.

Playing super mario 64 on our vita is no longer a meme \(well we could always use the daedalusX64 in adrenaline\) and you want to celebrate it by making a nice and shiny bubble you will pin in first page? But you're kind of lost in how to do that? Then you're in the right place !

## What do I need?

* A Vita \(ofc\)
* A Windows PC \(well, Linux and MacOS users can always try to use wine, catalina users will have to use bootcamp\)
* A rom of your game
* DaedalusX64 already working \(with the data files\)
* The builder files \(In release tab, you will have to download the builder.zip and extract it somewhere\)

## Ok got it, which exe should I launch?

Nope, no exe. It's a command line tool. The file you will need to launch is the build.bat

You will have a nice cmd window asking you 3 things \(don't worry, it's not some hacker stuff nor complicated command line process like hencore\)  


* Name of the vpk : Either simple like supermario64 or something fancy like peachgotcapturedagainpart4 if you like.
* The name of the rom : if the rom name is sm64.n64 then write sm64.n64
* The title ID : Up to you, it must be 9 letters and numbers in uppercase DAEDALUS3 is correct, SuPeRmArIo isn't because it's not 9 characters and not full uppercase.

Once it's done it will generate a vpk that you can install on your vita and that's all you have to do to have a custom bubble !  


## That's nice and all, but i don't want another daedalus bubble, I want a super mario themed bubble

Yeah ok it's all grey it's not fun we got it. Well you can customize the background and the icon app If you want. You must respect the following rules :

* Background picture is a png file and its dimension is 840x500. Name of the file : bg.png
* Icon picture is a png file and its dimension is 128x128. Name of the file : icon0.png
* Startup button icon is a png file and its dimension is 280x158. Name of the file : startup.png

Once it's done, you can put all of these png file in the asset folder and run again the build.bat, it will generate a vpk with your super mario themed bubble.

![Oh a Mario head](../.gitbook/assets/image.png)



![No vita? No problem, vita3K exist](../.gitbook/assets/image%20%283%29.png)

And that's it, you have a nice super mario themed bubble. I chosed super mario 64 as an exemple but you can do the same with any games you want.  
  


