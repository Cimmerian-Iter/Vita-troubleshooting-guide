---
description: 'Drugs are bad, but this one is good'
---

# Adrenaline

Finally, you got everything working, a hacked Vita, a working SD2Vita and your feel nostalgic. Want to play an epic, action game like Pursuit Force? Or play a Formula 1 game? Emulate Metal Gear Solid PSX? Then Adrenaline is for you! However, after installing it, Adrenaline decides to rebel against you and refuses to function? Let's see how to get it back on track.

## Adrenaline gives me an error about a 661.PBP

When you first launch Adrenaline, it will try to install the PSP firmware, because the PSVita has the PSP hardware in it \(thanks Sony\) and therefore it will need the 661.PBP firmware. You can download it from the Sony website or, if your PSVita is connected to internet, it can do it itself. If you prefer to do it manually, rename the `EBOOT.PBP` to `661.PBP` and put it in `ux0:app/PSPEMUCFW/` then start Adrenaline. It should now install the firmware and boot into PSP mode.

## I don't see the memory card in Adrenaline under game section

If you don't see the memory card icon in Adrenaline where you access it to have the list of PSP game you have, then the problem lies in the plugins. To be precise, the PSP plugins you have installed. Usually, CategoryLite is the main culprit. But if it's not that, then first deactivate all the PSP plugins in the `seplugins` folder, then see if you can see the memory card icon. If yes, activate the plugins one by one to search for the culprit. Once you identify it, get rid of it

## Adrenaline doesn't want to boot / I have an error code at boot

Try to delete Adrenaline and reinstall it. If that doesn't solve the problem, then it's most likely a corruption problem. If you are an SD2Vita user, then switch the positions: mount the memory card as `ux0` and the SD2Vita as `uma0`. Then try to install Adrenaline on it and see if it works. If yes, head to the Memory Corruption part to fix the problem on your MicroSD.

## I don't see my games

Make sure you have placed the PSP games in the right folder.  
PSP ISO and CSO in `ux0:pspemu/iso/`

PSX games and PSP homebrew in `ux0:pspemu/PSP/GAME/`

## I try to boot a PSX game but Adrenaline crashes.

I guess you used the PSX2PSP conversion tool. Well not every PSX game can be played. If they have a digital release in the PlayStation Store, then they are assured to be playable on the vita \(we usually prefer using the PSN digital version in that case\). If not, then it's a bit of a hit and miss. If it doesn't work, try converting the PSX game differently or using another dump of the game. If it still doesn't work, then we can't do much about it. If you are on 3.60 and don't mind the lack of sound you can try running the PSX game in Ark. \(How that you're wondering what it is? It's a PSP "emulator" like Adrenaline. You can use a tool like Ark Fast to install it on you PSVita\)
