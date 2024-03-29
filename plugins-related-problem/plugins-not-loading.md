---
description: halp they ate all my ram and now i can't breath
---

# Plugins not loading

Dealing with plugins is kind of annoying and hard to debug in some cases. If it bootloops, we need to find the culprit plugin(s) through a witch hunt. Fortunately, through previous community experience, we can narrow down the issue.



## Plugins are programs.

It may sound unrealistic but yeah. Plugins are microprograms that affect the system. You wonder why your phone/computer runs slowly when you have a ton of apps installed and running? Well it's the same case here. The more plugins you try to load, the more system resources they will need, like RAM. If it asks for too much, it will lead to a bootloop. That's why you should moderate yourself and not install all plugins you can find. (Someone once reached out to me because he couldn't boot his Vita after installing ALL the plugins he found in Autoplugin 2)

We will use an example on a common case I found during my time helping people:

```
# This file is used as an alternative if ux0:tai/config.txt is not found.
# For users plugins, you must refresh taiHEN from HENkaku Settings for
# changes to take place.
# For kernel plugins, you must reboot for changes to take place.
*KERNEL
ur0:tai/minivitatv.skprx
ur0:tai/ds3.skprx
ur0:tai/music_premium.skprx
ur0:tai/PSVshell.skprx
ur0:tai/storagemgr.skprx
ur0:tai/plugins/vitabright.skprx
ux0:app/PSPEMUCFW/sce_module/adrenaline_kernel.skprx
ur0:tai/plugins/nonpdrm.skprx
ur0:tai/ioplus.skprx
ur0:tai/AnalogsEnhancer.skprx
ur0:tai/NoPowerLimits.skprx
ur0:tai/0syscall6.skprx
ur0:tai/ds4vita.skprx
ur0:tai/udcd_uvc.skprx
# henkaku.skprx is hard-coded to load and is not listed here
# main is a special titleid for SceShell
ur0:tai/henkaku.suprx
*NPXS10015
# this is for modifying the version string
ur0:tai/henkaku.suprx
*NPXS10016
# this is for modifying the version string in settings widget
ur0:tai/henkaku.suprx
*main
ur0:tai/LowMemMode.suprx
ur0:tai/plugins/download_enabler.suprx
ur0:tai/plugins/shellbat.suprx
ur0:tai/volume_profile.suprx
ur0:tai/quick_volume.suprx
*ALL
ur0:tai/BackTouch2L2R2.suprx
ur0:tai/vitagrafix.suprx
ur0:tai/remaPSV.suprx
*NPXS10013
ur0:tai/ps4linkcontrols.suprx
```

That's a pretty big list there. It's no wonder why his Vita doesn't load anymore. Unfortunately, in most cases of bootloop the config looks like this. So, let's take this example and see how we solve it.

\*not talking about the fact that he put some plugins inside a plugins folder which is not recommended\*

## Installing multiple plugins that do the same thing

Yep, that's his first mistake. Let's take a closer look.\
This guy want to use his DS4 (PS4 controller enabler) plugins, but he loaded all the plugins for it: minitv, ds3 and ds4.\
He needs to make a choice, either use minitv or ds4. In this case let's go with minitv (which uses DS3 as a dependency)

## SD2VITA and ioplus plugin not being at the top.

Another common mistake is to not put the SD2VITA at the begining of \*KERNEL. This is very important as normally every plugin need to be loaded after the storage is mounted or else there will be problems upon boot because of the sudden storage change.\
As for ioplus it is a dependency used by other plugins to have access to more IO operation in userland. It needs to be loaded before them.

## Loading heavy plugins when we don't always use them

UCDCD's uvc plugin for streaming the PSVita screen through the USB is one of the most heavy plugins and need a lot of resources. If you want to use it, make some room for it. Let's see:

* I don't think you need to activate the music related plugins, that already removes 3 plugins from the list.
* PS4 link controls? Not useful in that case.
* Nopowerlimit, unless you really want to leave the WI-FI open while playing a game that disables it you can also remove this one
* Adrenaline plugin is one of the most useless plugins there. Just to avoid launching the app twice (one time to inject the adrenaline.skprx, and a second time to open adrenaline). Let's free our config from this one too.
* Using remap plugins, analog enhancer and BackTouch when we use a DS4 controller is also useless. It's just wasting memory at this point since you will use your PS4 controller and not the Vita control. We did some cleanup so let’s see what the config looks like

```
# This file is used as an alternative if ux0:tai/config.txt is not found.
# For users plugins, you must refresh taiHEN from HENkaku Settings for
# changes to take place.
# For kernel plugins, you must reboot for changes to take place.
*KERNEL
ur0:tai/storagemgr.skprx
ur0:tai/minivitatv.skprx
ur0:tai/ds3.skprx
ur0:tai/ioplus.skprx
ur0:tai/PSVshell.skprx
ur0:tai/vitabright.skprx
ur0:tai/nonpdrm.skprx
ur0:tai/0syscall6.skprx
ur0:tai/udcd_uvc.skprx
# henkaku.skprx is hard-coded to load and is not listed here
# main is a special titleid for SceShell
ur0:tai/henkaku.suprx
*NPXS10015
# this is for modifying the version string
ur0:tai/henkaku.suprx
*NPXS10016
# this is for modifying the version string in settings widget
ur0:tai/henkaku.suprx
*main
ur0:tai/LowMemMode.suprx
ur0:tai/download_enabler.suprx
ur0:tai/shellbat.suprx
*ALL
ur0:tai/vitagrafix.suprx
```

It looks way cleaner now. As you have seen, people always tend to load more plugins than they really need. Using only the plugins you need for the game session you will do allows you to enjoy your system without being blocked by a bootloop. You can create multiple config.txt's for each case if you want as long as the config isn't heavy (more than 10 plugins at the same time is not recommended).\
By following the same logic you can clear your config.txt easily without scratching your head over why it won't boot.

Note: If vitabright doesn't work for you even though you did what I told you to do, then look at this: [https://github.com/devnoname120/vitabright/issues/13](https://github.com/devnoname120/vitabright/issues/13)

## Using Easy Switch Vita

An app was made so that if you use the uvc plugin, you could control what plugins were enabled when you connected the Vita to a big screen, or disabled when you're using it as a handheld. [You can get it here](https://vitadb.rinnegatamante.it/#/info/398)

