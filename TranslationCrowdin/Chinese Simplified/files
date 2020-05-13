---
description: where is my data reeeeeeeee
---

# Memory corruption

Memory corruption is also a frequent problem while dealing with the PSVita because of how it handle FAT function. Guess that's why we also have a Content Manager and a database for the PSVita because sony knew that there was a problem and that the PSVita can corrupt the storage \(also explain why some memorycard doesn't have a good lifetime\) If you use a SD2Vita, and you experience some weird problems like your PSVita freezing or when you try to launch a game/app and it says the app is corrupted you can easly solve the problem.

## All my apps say they are corrupted. And i don't have Enso.

If you use a sd2vita without Enso and you experience this problem it's normal. When you will mount the SD2VITA while launching the hack, the system will change the storage in ux0 but won't refresh the live area so the bubbles of the app installed in the memorycard will remain even if you hadn't installed it in the SD2VITA. So naturally as you don't have the files \(or didn't put them correctly in the SD2VITA\) the app will give you a corruption error message. Do yourself a favor and downgrade to 3.60 and install Enso for the optimal SD2VITA experience.

## I have imported my music with Media Importer and when i try to play a music it says it's corrupted.

That's one of the problem of not using the Content manager to import the music. When you import the music from Media Importer and then close and reopen the music app after playing some music it will give you this error. We can't do anything besides rebooting to solve this issue. Everytime you will close the music app it will give you that error if you try to open it again.

## I have a 256G SD2VITA and everytime i try to open an app it gives me an error.

On that case it's usually a cluster size problem. You most likely didn't use 64kb in the format settings. Try again.

## I have a corruption on a specific app/music, my vita tend to freeze

Well that's what i depicted in the introduction. So grab your pc we will run some commands to fix it.

Windows users : Open Powershell or CMD as admin and input this command

```bash
chkdsk /F f: #assuming f is the letter associated to your microsd (Not the first F ofc)
```

Linux users : Open a terminal and write this command

```bash
sck.fat -a /dev/(device) #replace device with the correct name of your microsd mountpoint
```

> Most common ones are `Directory has non-zero size` after you save a game, and `Start does not point to ..` after you install a game, DLC or update by official means. If you delete something, you will get free cluster mismatch.  
> Credit : u/pthfdr on r/vitahacks

After doing this, insert the microsd in your vita and reboot. The problems should fade away.

