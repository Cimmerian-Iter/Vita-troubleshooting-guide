---
description: Cloud Gaming FTW
---

# Load Rom through a web server

Even though we now have sd2vita that gave us new storage possibilites so that we never run out of space, loading rom through a local server on the pc can be more convenient. It's more accessible and you can easly manage your rom instead of having to download and transfer to vita through usb/ftp.  
And you can play on the go ! This guide will cover how to create a web server in your pc using the software Apache \(Available in Windows, Mac and Linux\) with the required files.

## 1 Setup Apache

Although I always recomment to manually install the softwares to have a better understanding of how things work \(and especially for software like webserver to understand their structure and their functioning\) in this case I will directly link to a .msi so that anyone can install it in 2min. If you want to customize the path of the server, change port etc, you can check [this guide](https://www.sitepoint.com/how-to-install-apache-on-windows/)  
  
You can find the .msi [here](https://archive.apache.org/dist/httpd/binaries/win32/) \(Yeah there is a lot of files, you need to download apache latest version available win32 x86.msi At this time the one I downloaded is :

```text
apache_2.2.9-win32-x86-openssl-0.9.8h-r2.msi 
```

Once done, install the .msi like any windows application. Chose the normal installation. Once it's done, you will have no Apache application. Just a pop up in the task bar called Apache monitor, which will open a monitor to start/stop the webserver.

To ensure that the webserver is properly setup and working, open a browser and write `http:localhost`

![Indeed it works](../../.gitbook/assets/image%20%284%29.png)

What we need now is to locate the root of the webserver.   
  
With a normal installation it's in : `C:\Program Files (x86)\Apache Software Foundation\Apache2.2\htdocs`

This is where we will drop the rom as well as the configuration file : htaccess \(Download and drop it in htdocs\)

![Delete index.html after checking that the webserver works by showing &quot;It works&quot;. Don&apos;t mind token.html](../../.gitbook/assets/image%20%286%29.png)

Once this is done, we need to know the IP of your computer. Not a hard task, open a cmd windows and write : `ipconfig`

You should easly notice your local IPv4 address

![If a hacker pass by pls don&apos;t hack my IP address](../../.gitbook/assets/image%20%287%29.png)

## 2 Access the local webserver with Daedalusx64

Open the Option tab and write the address of your pc in web server like that : `http://yourpcip`

![My IP is 192.168.0.15 so i write http://192.168.0.15](../../.gitbook/assets/image%20%285%29.png)

Once done, it should show the rom on the menu like that : 

![Time for some peach daily saving.](../../.gitbook/assets/image%20%288%29.png)

And that's it, you can add as much rom as you want, make the whole N64 library if you want on your pc. And if you tweak Apache, you can make a webserver that would allow to connect to it without being in the same network. Like being in a hotel in Paris and access rom located in your pc in Japan. 

