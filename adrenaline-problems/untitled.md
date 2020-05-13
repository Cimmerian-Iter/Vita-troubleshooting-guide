---
description: 'Drugs are bad, but this one is good'
---

# Adrenaline

Finally, you got everything working, a hacked vita, a working SD2VITA and you feel nostalgic. Want to play an epic, action game like Pursuit Force? Or play an F1 game? Emulate Metal Gear Solid PSone? Then Adrenaline is for you. 
But after installing it decide to go against you and doesn't want to work? Let's see how to make it work.

## Adrenaline gives me an error about a 661.PBP

When you first launch adrenaline, it will try to install the PSP firmware, because the PSVita has the PSP hardware in it \(thanks Sony\) and therefore it will need the 661.PBP firmware. You can download it from the Sony website or, if your PSVita is connected to internet, it can do it himself. if your prefere to do it manually, rename the `EBOOT.PBP` to `661.PBP` and put it in `ux0:app/PSPEMUCFW/` then start Adrenaline.It should now install the firmware and boot into PSP mode.

## I Don't see the memory card in Adrenaline under game section.

If you don't see the memory card icon in Adrenaline where you access it to have the list of PSP game you have, then the problem lies in the plugins. To be precise, the PSP plugins you have installed. Usually categorylite is the main culprit. But if it's not that, then first deactivate all the PSP plugins in the `seplugins` folder, then see if you can see the memorycard icon. If yes, then activate the plugins one by one to search for the culprit. And get rid of it

## Adrenaline doesn't want to boot: I have an error code at boot.

Try to delete Adrenaline and reinstall it. If that doesn't solve the problem, then it's most likely a corruption problem. If you are an SD2VITA user, then switch the positions : mount the memorycard as `ux0` and the SD2VITA as `uma0`. Then try to install Adreanline on it and see if it works. If yes, then head to the Memory Corruption part to fix the problem on your microSD.

## I don't see my games

Make sure you have placed the PSP games in the right folder.  
PSP ISO and CSO in `ux0:pspemu/iso/`

PSOne games and PSP homebrew in `ux0:pspemu/PSP/GAME/`

## I try to boot a PSone game but Adrenaline crashes.

I guess you used the PSX2PSP conversion tool. Well not every PSone game can be played. If they have a digital release in the PlayStation Store, then they are assured to be playable on the vita \(we usually prefer using the PSN digital version in that case\). If not then it's a bit of a hit and miss. If it doesn't work then try converting the PSone game differently or using another dump of your PSone game. If it still doesn't work then we can't do much about it. If you are on 3.60 and don't mind the lack of sound you can try running the PSone game in Ark. \(How that you're wondering what it is? It's a PSP "emulator" like Adrenaline. You can use a tool like Ark Fast to install it on you PSVita\)

