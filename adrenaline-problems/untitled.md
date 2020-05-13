---
description: 'Drugs are bad, but this one is good'
---

# Adrenaline

Finally, you got everything working, a hacked vita, a working SD2VITA and you feel nostalgic? Want to play some epic actions game like Pursuit Force? Or play some F1 games? Emulate MGS psone? Then adrenaline is for you. But after installing it decide to go against you and doesn't want to work? Let's see how to make it work.

## Adrenaline gives me an error about a 661.PBP

When you first launch adrenaline, it will try to install the PSP firmware, because yeah the PSVita has the PSP hardware in it \(Thanks Sony\) and thus it will need the 661.PBP firmware. You can download it from the sony website. Rename the EBOOT.PBP to 661.PBP and put it in ux0:app/PSPEMUCFW/ then start adrenaline. Should now install the firmware and boot into the PSP mode.

## I Don't see the memorycard in adrenaline under game section.

If you don't see the memorycard icon in adrenaline where you access it to have the list of PSP game you have, then the problem lies in the plugins. To be precise, the PSP plugins you have installed. Usually categorylite is the main culprit. But if it's not him then first desactivate all the PSP plugins in seplugins folder, then see if you can see the memorycard icon. If yes, then activate the plugins one by one to search for the culprit. And get ride of it

## Adrenaline doesn't want to boot i have an error code at boot.

Try to delete adrenaline and reinstall it. If it doesn't solve the problem. Then it's most likely a corruption problem. If you are a SD2VITA user, then switch the positions : mount the memorycard as ux0 and the SD2VITA as uma0. Then try to install adreanline in it and see if it works. If yes then head to the Memory Corruption part to fix the problem on your microsd.

## I don't see my games

Make sure you have placed the PSP games in the right folder.  
PSP ISO and CSO in ux0:pspemu/iso/

PSONE games and PSP homebrew in ux0:pspemu/PSP/GAME/

## I try to boot a PSONE game but adrenaline crash.

I guess you used the PSX2PSP conversion tool. Well not every PSONE game can be played. If they have a digital release in PSTORE, then they are assured to be playable in the vita \(we usually prefer using the PSN digital version in that case\). If not then it's a hit and miss. If it doesn't work then try converting the PSONE game differently or using another dump of your PSONE game. If it still doesn't work then we can't do much about it. If you are on 3.60 and don't mind the lack of sound you can try running the PSONE game in ark. \(How that you're wondering what it is? It's a PSP "emulator" like adrenaline. You can use a tool like Ark Fast to install it on you PSVita\)

