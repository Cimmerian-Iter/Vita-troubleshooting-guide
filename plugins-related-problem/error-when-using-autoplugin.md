---
description: robot does break
---

# Error when using autoplugin/How to correctly install plugins

#### Sometimes, autoplugin will fail, we know that autoplugin 1 tends to corrupt the config.txt \(and recently autoplugin 2 also corrupting the config.txt although the issue has been solved in 1.05 as of today\) It is importantly to know how to deal with plugins. Autoplugin is a great homebrew, but it shouldn't replace totally the knowledge of plugins and you can't expect it to be fail-proof. So we will see how can we recover from autoplugin misbehavior by learning about how tweaks works.

## What is a plugin?

you may have already encountered it through the PSP area, plugins are micro programm that runs in background and enhance your experience. It's purpose can be various like dealing witht the overclock, modification of the live area or native function \(like the screenshot or music player\). They are essentials nowadays. They are loaded by the framework Taihen thanks to the effort of the Molecule Team.  
There is two types of plugins.

SKPRX : those are kernel plugins, most commons nowadays, it modify the overall functions of the vita. Like nonpdrm fake the drm system, storagemgr load the sd2vita as a memorycard, and more. They need a reboot between the installation to run. \(Or use xerpi plugin loader\)

SUPRX : those are users plugins, we can split this group into two : those which modify the live area \(\*main\) system behavior, and those which modify the in-game/app \(\*ALL\) behavior. To know which category the plugin you have belongs, you either need to know what it does, or just read the github description \(they often tell you if you need to install it under \*main or \*ALL\)  
They don't need a reboot to be loaded, reloading taihen config in henkaku settings should do the job.

## How do i install a plugin?

This part isn't really difficult. It is quite easy in fact. All you need to do is to write some lines.

To install plugins you need to do 2 things :

### Place the plugin file in ur0:tai folder \(or ux0:tai if you want to use ux0\)

Plugins belongs to the tai folder where the config.txt is. There may be some exeption like vitacheat.suprx which need to be in it's vitacheat folder in ux0

### Write the path to the plugin in the config.txt

The path is the location of the file. If the plugin is located in ur0:tai, then the path is : ur0:tai/name.skprx  
You need to write the path in the config.txt under the category of the plugin.  
KERNEL : skprx  
MAIN : live area tweak  
ALL : apps tweak

Here an exemple. Let's imagine i have a tai folder in ur0 that contain  
KERNEL : storagemgr.skprx, lolicon.skprx, nonpdrm.skprx  
MAIN : shellbat, download enabler  
ALL : vitacheat \(skprx is in ur0:tai/, suprx is in ux0:vitacheat/\)

```bash
*KERNEL
ur0:tai/storagemgr.skprx
ur0:tai/lolicon.skprx
ur0:tai/nonpdrm.skprx
ur0:tai/vitacheat.skprx

*main #main needs to be in lowercase
ur0:tai/shellbat.suprx
ur0:tai/download_enabler.suprx

*ALL
ux0:vitacheat/vitacheat.suprx
```

You can also specify which app will load the plugin, for exemple if you want to enable vitacheat only in certain game, you need to write the path of the file under the code name of the app. To know the code name of the app, either you look with vitashell for the code name of the homebrew in ux0:app \(often easy to guess with the names\), or you google the code name of the game you want. For testkit users, you can easly know the code name of an app by showing the information of the app in the live area.  
Additionally, you can specify which app will not load the plugin. It can be useful for exemple when your overclock tweak crash adrenaline. To do that, you need to add a ! before the code name.

Here's an exemple, i want to enable vitacheat in killzone only, and i don't want to load lolicon in adrenaline.

```text
*PCSF00243
ux0:vitacheat/vitacheat.suprx

*!PSPEMUCFW
ur0:tai/lolicon.skprx
```

### Note :

1 If you use a sd2vita, ux0:tai MUST NOT exist. Delete it and put every plugins in ur0:tai.  
The sd2vita plugin you use always need to be at the top of \*KERNEL, else the other plugins won't work correctly.

2 Be aware that plugins have an impact, if you load too much plugins, you can expect some lags or in the worst case, a bootloop. That is especially true if you tend to have more than 10 plugin, or load xerpi usb screenshare plugin \(which is heavy\) with a lot of plugins.

Try to load only the necessary plugins. If your vita bootloop, you can for enso users hold L button when booting to avoid loading plugins, or for 3.67+ open hencore and do a reset taihen.

3.65 enso users might have to format their memorycard if id.dat is still in the memorycard \(the file that indicate the firmware and the psn account of the user\) and since we unload the plugins, we also disable the firmware spoof, so when the vita will read that file, it will ask you to update in order to use it or format it. You will have no other choice but to format or update to 3.73 \(at this time\). 3.60 users can always reset henkaku through the webkit exploit without formating the memorycard \(you will boot in a blank livearea\) and unlink the memorycard through henkaku settings, but for 3.65 users since you don't have access to the memorycard you won't be able to reset taihen \(Another reason why i recommend everyone to go to 3.60\).

You can always come in the henkaku server discord if you want more information about plugins or contact me directly.

