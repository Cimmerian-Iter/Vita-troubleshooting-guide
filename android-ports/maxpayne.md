---
description: 'No payne, no gain'
---

# MaxPayne

Since Rockstars decided to just skip the PSVita and focus on Android why not do it ourselves? After the GTA series \(2D and 3D era\) that is entirely ported to the PSVITA, thanks to a co effort from fgsfdsfgs and TheFlow, we can play the Android version on Vita with a .so wrapper \(kind of like wine does for linux\)

## What do I need?

* The game obviously. Don't go installing the vpk and expect having the full game. First download the game on your phone. And if like me you're an iOS \(masterace\) User, then you can install Bluestack \(Android emulator easy to use\) to download the game on your PC directly. 
* The vpk and data.zip from the [github](https://github.com/fgsfdsfgs/max_vita/releases)
* Around 1.8GB of data of free space
* [kubridge](https://github.com/TheOfficialFloW/kubridge/releases/), libshacccg and [fdfix](https://github.com/TheOfficialFloW/FdFix/releases)
* Patience. I'm not joking you need to follow the steps closely.
* This guide

## Kubridge? libshacccg? fdfix?

Make sure you have **libshacccg** in ur0:data, if you don't have it then follow [that guide](https://samilops2.gitbook.io/vita-troubleshooting-guide/shader-compiler/extract-libshacccg.suprx) to have it 

As for **Kubridge** \(lift some restrictions on some memory management\) and **fdfix** they are 2 essential plugins you need. \(If you are a **Repatch user**, then don't install fdfix. Repatch also does fix the file descriptors being invalidated after suspend and resume leading to some homebrew/ports crashing when you wake up the vita\).  


Download the 2 plugins and put them in the tai folder you use \(If you don't know how to install plugins, then check the how to install plugin section\)  
  
Then write those 2 lines under the \*KERNEL in the config.txt \(in case you put them in ur0:tai\)

```text
*KERNEL
ur0:tai/kubridge.skprx
ur0:tai/fd_fix.skprx
```

Remember that you need to respect some conventions with plugins, like the sd2vita plugins always at the top of the Kernel section.  
Once it's done you can reboot.  


## Ok I have the game installed on my phone, how do I transfer it?

Once you paid the game and installed it on your phone we will need to have the apk and the obb.  
The obb isn't hard to get, it's located in `/sdcard/android/obb/com.rockstar.maxpayne/main.3.com.rockstar.maxpayne.obb`

As for the apk it's different.  
Either you're a hackerman and know how to use adb, you can follow [this ](https://stackoverflow.com/questions/11012976/how-do-i-get-the-apk-of-an-installed-app-without-root-access)  
If using a terminal scares you and you never scrolled in the settings app, then just install [this app](https://play.google.com/store/apps/details?id=com.ses.app.apkexport&hl=fr&gl=US) on your phone to extract the apk of the game.  
  
Once you have the two files, put them somewhere on your pc. We will work with those 2 files.

## So do I rename .apk to .vpk and install it?

Well yes but actually no.  
Apk is like vpk, it's a zip file so rename .apk to .zip and open it with whatever tool you usually use to extract the assets folder  
  


![Yeah you see that ass ets folder?](../.gitbook/assets/image%20%2812%29.png)

Once you have extracted the assets folder, rename it to maxpayne and send it to your vita.  
It should be there

```text
ux0:data/maxpayne
```

Then we will need the .so library, you can find it there : `lib/armeabi-v7a/libMaxPayne.so`

![MaxPayne.so](../.gitbook/assets/image%20%2815%29.png)

Take that file and put it inside the maxpayne folder in your psvita

Now we need to extract the contents of the obb files. No need to google obb extractor on google, the obb file is just a zip. So same as for the apk, rename it to zip

![ras = rien a signaler and msf = militaire sans fronti&#xE8;re](../.gitbook/assets/image%20%2814%29.png)

You can extract all of those files to the maxpayne folder again. And if you want to save some extra MB you can delete some files  
  
- Keep the v2.msf \(english\) and the msf of your language \(For example I'm french I will keep MaxPayneSoundsFrenchv2.msf\) and delete the others .msf that you don't need.  
  
NOTE : some obb ship the japanese sound bank as `MaxPayneSoundsJapanesev2`. If you want to use the japanese voices then rename it to `MaxPayneSoundsJapanesev3`

Once it's done you can now extract the maxpayne folder from the data.zip you have downloaded from the github to the root of the ux0:data folder \(Overwrite files if asked\)

 And you should have everything you need in order to make it run! Now install the vpk and play the game.  
If the game crash at boot make sure you have everything in place.  
  
For exemple : 

![french powa](../.gitbook/assets/image%20%2813%29.png)

