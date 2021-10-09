---
description: where is my data reeeeeeeee
---

# Memory corruption

Memory corruption is also a frequent problem while dealing with the PSVita because of how it handles FAT function. Guess that's why we also have a Content Manager and a database for the PSVita because Sony knew that there was a problem and that the PSVita can corrupt the storage \(also explains why some MemoryCards do not have a good lifetime\) If you use a SD2VITA, and you experience some weird problems like your PSVita freezing or when you try to launch a game/app and it says the app is corrupted you can easily solve the problem.

## All my apps say they are corrupted and I don't have Enso.

If you use a SD2VITA without Enso and you experience this problem, it's normal. When you mount the SD2VITA while launching the hack, the system will change the storage in ux0 but won't refresh the home screen so the bubbles of the app installed in the memorycard will remain even if you hadn't installed it in the SD2VITA. So naturally as you don't have the files \(or didn't put them correctly in the SD2VITA\) the app will give you a corruption error message. Do yourself a favour and downgrade to 3.60 and install Enso for the optimal SD2VITA experience.

## I have imported my music with Media Importer and when I try to play a music it says it's corrupted.

That's one of the problems of not using the Content Manager to import the music. When you import the music from Media Importer and then close and reopen the music app after playing some music it will give you this error. We can't do anything besides rebooting to solve this issue. Every time you close the music app it will give you that error if you try to open it again.

## I have a 256G SD2VITA and every time I try to open an app it gives me an error.

On that case, it's usually a cluster size problem. You most likely didn't use 64kb in the format settings. Try again.

## I have a corruption on a specific app/music, my Vita tends to freeze

Well, that's what I depicted in the introduction. So, grab your PC we will run some commands to fix it.

Windows users: Open Powershell or CMD as admin and input this command

```bash
chkdsk /F f: #assuming f is the letter associated to your MicroSD (Not the first F ofc)
```

Linux users: Open a terminal and write this command

```bash
sck.fat -a /dev/(device) #replace device with the correct name of your MicroSD mountpoint
```

> Most common ones are `Directory has non-zero size` after you save a game, and `Start does not point to ..` after you install a game, DLC or update by official means. If you delete something, you will get free cluster mismatch.  
> Credit : u/pthfdr on r/vitahacks

After doing this, insert the MicroSD in your Vita and reboot. The problems should fade away.

