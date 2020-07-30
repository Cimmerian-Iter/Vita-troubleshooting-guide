---
description: The worst ennemy of the PSVita
---

# QCMA

You struggle with QCMA? Can't manage to connect to your PC? You're most likely facing a driver issue. We usually need prefer connecting the Vita through wifi with QCMA to avoid problems since it's used mostly for transfering H-encore to the PSVita. But if you need to connect your PSVita through usb \(for FW reinstallation or to make a backup that would take ages to complete through wifi because PSVita wifi chip is limited to 8mb/s\) then let's see how we can solve this.

Note : Everything here is destined for Windows users. Mac user have already the best OS when it comes to program installation and doesn't have any problems. Linux users shouldn't face too much problems neither.

## 1 Make sure you don't have CMA installed

If you already installed it then it will conflict with QCMA, so you won't be able to successfully connect to the PC. Delete the drivers installed with the PSVita too.

## 2 Delete the drivers manually and reinstall it.

For that we will do in 2 step. The first one is to delete the driver of the PSVita using the device manager in windows, then try to find the PSVita device. It should look like that :

![Get ride of this bad boy](../.gitbook/assets/adda.PNG)

Right click on it, go to propreties, then uninstall the device \(make sure you tick the delete the driver box\)

Second step is to download the software zadig \(no virus garantee\) You can get it [there](https://zadig.akeo.ie/).

Once you have installed the app and run it, list all the devices and select the PSVita \(make sure the PSVita is connected ofc\).

![First enable the list All devices option](../.gitbook/assets/addaa.PNG)

As for the driver, we had better luck with libusbk so install it with zadig.

![Sorry WinUsb, you won&apos;t be missed](../.gitbook/assets/li.PNG)

Press the install button and it should be good. Reboot your pc and connect the vita and QCMA should connect fine to the Vita.

Note : On a very rare occasion even after doing these steps. QCMA won't connect to the vita. You can try to use the official CMA from sony \(For cases like if you want to reinstall the firmware. It does the job\) Or take a virgin PC and install QCMA on it

