---
description: 'welcome to the dark side, we have cookies'
---

# Bootloop/Brick. Let's reinstall the firmware

So you wanted to enjoy your vita and tried to do anything risky? \(testkit mod, downgrade, messing with system files\) and the only option available in safe mode is update the firmware? Or pressing L at boot doesn't help? No worry you can still save the PSVita, most of the bricks are actually recoverable. As long as it is software and you didn't wipe os0 \(unless you have enso ex\)

## So doctor? what's the solution?

First of all, what i always recommend is to put a pup file in ux0:data/PSP2/UPDATE/PSP2UPDAT.pup It avoid the need to connect with a pc and QCMA can be unreliable. You can then use it with option 5 update the system, and update from gamecard \(yeah yeah that option works with memorycard\). After you solve the problem, do that so next time it'll be easier.  
  
Try to do the battery reset combo \(which will reset the syscon. Can save some cases like it did for me.\)

press PWR+PS+SELECT+START+L for 15-20 secs then try to power on the PSVita  
  
In order to reinstall the firmware, we will update yep. "Update to 3.60" is the same thing as reinstall 3.60 as it will install the 3.60 pup. So let's begin, download the pup of your choice. Here's a little list.  


* 3.60 [https://yatsukiko.me/psvu/3.60/PSP2UPDAT.PUP](https://yatsukiko.me/psvu/3.60/PSP2UPDAT.PUP)
* 3.65 [https://yatsukiko.me/psvu/3.65/PSP2UPDAT.PUP](https://yatsukiko.me/psvu/3.65/PSP2UPDAT.PUP)
* 3.68 [https://yatsukiko.me/psvu/3.68/PSP2UPDAT.PUP](https://yatsukiko.me/psvu/3.68/PSP2UPDAT.PUP)
* UP TO DATE FW : go download it from sony and don't forget to rename it into PSP2UPDAT.PUP

Once you have downloaded the pup, make sure you have qcma installed, and put the pup file in the update directory. \(look in qcma settings where is the update foledr. Usually called PSV updates.\)  
  
And change qcma settings about the firmware to avoid the "you already have the latest version" message

![Check ignore local file psp2updatlist and change the FW version](../.gitbook/assets/klk.PNG)

You need to change the "FW : up to date" in use this version for updates into : custom.  
Then in the custom PS Vita version field write the corresponding version to the target firmware

* 3.60 : 03.600.000
* 3.65 : 03.650.000
* 3.73 : 03.730.000

And if you understood the logic you can adapt it for futur updates.

That's it on pc side. Now connect your vita through USB mode and do the option 5 : Update this system and chose update from PC and you should be reinstalling the firmware now.   
  
If you have troubles making QCMA recognize your vita, head to the qcma section to know how to fix the errors.  
  
Once you have reinstalled the firmware, redo the hack and it should be good now.

