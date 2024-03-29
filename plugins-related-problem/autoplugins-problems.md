# Error when using Autoplugin

#### Sometimes, Autoplugin will fail and we know that Autoplugin tends to corrupt the config.txt. It is importantly to know how to deal with plugins. Autoplugin is a great homebrew, but it shouldn't totally replace knowledge of plugins and you can't expect it to be fail-proof. We will see how can we recover from Autoplugin misbehavior by learning about how tweaks works.

## What is a plugin?

You may have already encountered it through the PSP era, plugins are micro programs that runs in background and enhance your experience. Their purposes can be various like dealing with overclocking, modification of the livearea or a native function \(like the screenshot or music player\). They are essentials nowadays. They are loaded by the framework TaiHEN thanks to the effort of the Team Molecule.  

There are two types of plugins.  
  
SKPRX: These are kernel plugins, most common nowadays, it modifies the overall functions of your PSVita. Like nonpdrm to fake the drm system, YAMT to load the SD2VITA as a MemoryCard, and more. They need a reboot between the installation to run. \(Or use xerpi's plugin loader\)  
  
SUPRX: these are users plugins, we can split this into two groups. Those which modify the live area \(\*main\) system behaviour, and those which modify the in-game/app \(\*ALL\) behaviour. To know which category the plugin you have belongs, you either need to know what it does, or just read the Github description \(they often tell you if you need to install it under \*main or \*ALL\)  
They don't need a reboot to be loaded, reloading the taiHEN config in HENkaku settings should do the job.  
  


## How do I install a plugin?

This part isn't really difficult. It is quite easy in fact. All you need to do is to write some lines.  
  
To install plugins you need to do 2 things:

### Place the plugin file in ur0:tai folder \(or ux0:tai if you want to use ux0\)

Plugins belongs to the tai folder where the config.txt is. There may be an exception like vitacheat.suprx where it needs to be in it's own vitacheat folder in ux0

### Write the path to the plugin in the config.txt

The path is the location of the file. If the plugin is located in ur0:tai, then the path is : ur0:tai/name.skprx  
You need to write the path in the config.txt under the category of the plugin.  
KERNEL: .skprx  
MAIN: Bubble Launcher tweaks  
ALL: App tweaks  
  
Here an example. Let's imagine I have a tai directory in ur0 that contains:  
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

  
You can also specify which app will load the plugin, for example if you want to enable vitacheat only in certain game, you need to write the path of the file under the code name of the app. To know the code name of the app, either you look with vitashell for the code name of the homebrew in ux0:app \(often easy to guess with the names\), or you Google the code name of the game you want. For testkit users, you can easly know the code name of an app by showing the information of the app in the live area.  
Additionally, you can specify which app will not load the plugin. It can be useful for example when an overclock tweak crashes Adrenaline. To do that, you need to add a ! before the code name which stops the plugin running when opening the specified app.  
  
Here's an example, I want to enable vitacheat in Killzone only, and I don't want to load lolicon in adrenaline.  


```text
*PCSF00243
ux0:vitacheat/vitacheat.suprx

*!PSPEMUCFW
ur0:tai/lolicon.skprx
```

###  Note : 

1. If you use a SD2VITA, ux0:tai MUST NOT exist. Delete it and put every plugins in ur0:tai.  
The SD2VITA plugin you use always need to be at the top of \*KERNEL, else the other plugins won't work correctly. The reason you'll have to do this is that when you load the SD2VITA plugin from ux0, it will swap the ux0 directory for your SD2VITA's. The problem is that it tries to acess the plugin again but since ux0 has been swapped it can't find the plugin.

2. Be aware that plugins have an impact, if you load too many plugins, you can expect some lags or in the worst case, a bootloop. That is especially true if you tend to have more than 10 plugins, or load xerpi usb screenshare plugin \(which is heavy\) with a lot of plugins.  
  
Try to load only the necessary plugins. If your vita bootloop, you can for enso users hold L button when booting to avoid loading plugins, or for 3.61+ open hencore and do a reset taihen.  
  
3.65 enso users might have to format their memory card if id.dat is still in the MemoryCard \(the file that indicate the firmware and the PSN account of the user\) and since we unload the plugins, we also disable the firmware spoof, so when the vita will read that file, it will ask you to update in order to use it or format it. You will have no other choice but to format or update to 3.73 \(at this time\). 3.60 users can always reset HENkaku through the WebKit exploit without formating the MemoryCard \(you will boot in a blank livearea\) and unlink the MemoryCard through HENkaku settings, but for 3.65 users since you don't have access to the MemoryCard you won't be able to reset taiHEN. \(Another reason why I recommend everyone to go to 3.60\)

