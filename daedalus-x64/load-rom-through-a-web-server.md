---
description: Cloud Gaming FTW
---

# Load Rom through a web server

Despite the fact we have the SD2Vita which gave us new storage possibilities meaning we rarely, if ever, run out of space, loading roms through a local server on the PC can be more convenient. It's more accessible and you can easily manage your roms instead of having to download and transfer to vita through USB/FTP. And you can play on the go! This guide will cover how to create a web server on your PC using the software Apache (Available on Windows, Mac and Linux) with the required files.

## 1 Setup Apache

Although I always recommend to manual installation of software in order to have a better understanding of how things work (and especially for software like webservers to understand their structure and their functions) in this case I will directly link to a .msi so that anyone can install it in 2 minutes. If you wish to customize the path of the server, change the port etc. You can check [this guide](https://www.sitepoint.com/how-to-install-apache-on-windows/).

You can find the .msi [here](https://archive.apache.org/dist/httpd/binaries/win32/) (Yeah there is a lot of files, you need to download Apache’s latest version available. win32 x86.msi. At the time of writing the one I downloaded is:

```
apache_2.2.9-win32-x86-openssl-0.9.8h-r2.msi 
```

Once the download has completed, install the .msi like any Windows application. Choose the normal installation. Once it's done, you will have no Apache application. Just a pop up in the taskbar called Apache monitor, which will open a monitor to manage the webserver.

To ensure that the webserver is properly setup and working, open a browser and input 'http:localhost\` into the URL bar.

![Indeed it works](<../.gitbook/assets/image (4) (1).png>)

The next task is to locate the root of the webserver.

With a default installation it's in: `C:\Program Files (x86)\Apache Software Foundation\Apache2.2\htdocs`

This is where we will drop the rom(s) as well as the configuration file: htaccess (Download and drop it in htdocs)

![Delete index.html after checking that the webserver works by showing "it functions". Don't mind token.html](<../.gitbook/assets/image (6) (1).png>)

Once this is done, we need to know the IP of your computer. Not a hard task, open a cmd windows and input: `ipconfig`

You should easily notice your local IPv4 address

![If a hacker happens to pass by plz don't hack me](<../.gitbook/assets/image (7) (1).png>)

## 2 Access the local webserver with Daedalusx64

Open the Options tab in the top left and input the IP address of your PC in webserver like this: `http://yourpcip`

![My IP is 192.168.0.15 so I wrote http://192.168.0.15](<../.gitbook/assets/image (5) (1).png>)

Once done, it should show the rom(s) on the menu like seen bellow:

![Time for some Peach’s daily saving.](<../.gitbook/assets/image (8) (1).png>)

And that's it. You can add as many roms as you want. Add the whole N64 library if you want on your PC. And if you tweak Apache, you can make a webserver that would allow to connect to it without being in the same network. Like being in a hotel in Paris and accessing your rom library located on your PC in Japan.
