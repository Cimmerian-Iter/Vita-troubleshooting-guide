---
description: i don't want to buy 100$ for 64G pls help
---

# SD2VITA doesn't work

You finally got ride of your little sony expensive memorycard and want to use that fresh SD2VITA you just bought 3bucks on Alie Express? But when you insert it into the vita it just doesn't works? Don't worry i'll cover the usual solutions to solve this.

## 1 Did i install the plugin the right way?

This is the most common case. Usually people buy a SD2VITA as soon as they begin to hack their vita and they don't set the plugin correctly. And we can check that. If you're using storage manager, there's a way to know if it is running or no. Check ur0:tai/storagemgrlog.txt if it exist. If it doesn't then you didn't install the plugin correctly so head back to the plugin section and try to redo it.  
If it exist then go to the next step.

Note for YAMT-Lite users :

* Only run the app once \(each time you will run it it will install/uninstallà\)
* Do not let it active when you want to insert a Gamecard instead of a SD2VITA

## 2 Did i format the microsd according to the guide?

Another common issue, is that storagemgr can't read the SD2VITA, open the log.txt file and look for the GCD detection part.  
If you see "GCD NOT DETECTED" in the log, then that means it couldn't read the SD2VITA.  
There is 2 reason, you are the culprit or the SD2VITA is the culprit \(there's always a small chance of you getting a bad build but it happened a lot in the community, the only solution is to buy another. We can't tell you a reliable source and we can't know in advance if the SD2VITA is well made or no. Although V6 exist for that purpose\).

To see if you are the culprit, then let's try formating the microsd again.  
Redo the formating step in vita hacks guide : [https://vita.hacks.guide/storage-format-\(windows\)](https://vita.hacks.guide/storage-format-%28windows%29)  
If you're a mac user or a linux user, then don't follow that part and flash zzblank.img, it is only needed because windows doesn't format the microsd in a correct way for the vita. There's a linux section and mac section in the guide.

If mac user wants my own instruction for formating their microsd here's some command you will need to input in a terminal to format it correctly.

```bash
diskutil list #find your sdcard (should be something like /dev/disk2)
diskutil unmount /dev/disk2   sudo dd if=/dev/zero of=/dev/disk2 #don't forget to change disk2 to your disk number
# remove and reinsert storage device 
sudo newfs_exfat -R /dev/disk2 #for microsd up to 128GB (may need to remove and reinsert to see it in finder)
sudo newfs_exfat -R  -c 128 /dev/disk2  #for microsd starting from 256GB
#Copy contents over to memory card
```

If you followed the steps correctly and it still doesn't work, then try again with another microsd. If it still doesn't work, then it's fair to assume that you got a bad SD2VITA. And the only option left is to buy another one.

