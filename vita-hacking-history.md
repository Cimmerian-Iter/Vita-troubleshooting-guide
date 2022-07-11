---
description: WIP
---

# Vita Hacking History

## 2016 The release of HENkaku

\
This is it, after some teasing, the july 2016, HENkaku was released by Team Molecule. This mark the end of the sand walk as we have the first native hack that gives total control of the vita including installing homebrew directly on the livearea. The pain of using rejuvenate is replaced by a website you need to browse to hack the Vita. It's ironic considering how tough the security was described and that given how rejuvenate was, we thought that we would need another complicated hack in order to jailbreak the vita. This also opens the door for better homebrew support and we saw it with the release of multiple utilities like moonlight it wasn't able to play backups of game. It has received several updates to include the henkaku settings, fixing firmware spoofing after sony decided to fight back a little before stopping completely. You can find a changelog of HENkaku [here](https://yifan.lu/2016/08/27/henkaku-update/).

The fact that HENkaku used a website and was not permanent meant that if you reboot and you don't have wifi you wouldn't be able to hack your vita to launch homebrew. Fortunately xyz found a trick and included the HENkaku exploit inside the mail app of the vita which contains webkit inside. So we could trigger HENkaku while being offline. Just open the mail and boom hacked.

A contest was created by the four main hacking forum that is Wololo, PSX Place, PlaystationHax.it and Custom Protocol. It was named [GekiHEN](https://gekihen.customprotocol.com/en/) and helped a lot in attracting developers and shining a light on the Vita. Thanks to it we had many cool submissions that we even use today like the vita homebrew browser, custom themes manager and pfba. The contest was a success although the results were shadowed by Project Void which won the game category while being built with the official Sony SDK and not Vita SDK.\
\
\
__Yfanlu doesn't endorse piracy and decided to make the job harder for pirates by not giving out the necessary tools for it. But TeamFreek, composed of Mr.Gas, MajorTom and TheFloW, found a way to backup games and planned on releasing the Vitamin dumper. Unfortunately, a relative of either Mr.Gas or Major Tom who got access to the vpk betrayed their trust and leaked the program. Shortly after TheFloW decided not to release the V1.0 of Vitamin and considered quitting the scene (imagine if he did). Fortunately, after that incident, TheFloW changed his mind and released the V1.0 but Mr.Gas and MajorTom decided to leave permanently. It's a big shame as they were 2 promising members of the scene (and they were fellow French).

After Vitamin was released another program to dump games was released by a Chinese dev. The name? MaidumpTool.

The dumping process was simple, load the game files in the ram and let the vita decrypt it. It was a dirty method of dumping game and it did introduce several problems like save data corruption.

The two programs with the same goal in mind had many advantages and disadvantages.

Vitamin :

* Install games as vpk, you can keep the Henkaku Safe Mode to be sure that the vpk you install didn't contain malicious code in order to prevent the "HarryPotter.vpk" situation that happened after a random user took Silica memorycard eraser vpk and renamed it into harrypotter.vpk and shared it.
* You need to transfer the vpk to the vita and install it with vitashell. This means you need double the space to install a vpk. And it took ages to install a game. There were some other tricks like using vita organizer which install a vpk from your computer to your PSVita through ftp, or extracting game assets from the vpk, transferring it through usb to ux0:app then rezip the vpk with only sys\_info and eboot bin and install it with vitashell.

MaiDump :&#x20;

* Install games as a folder which means you don't need the double space to install a game. And you don't have the unzip part which means it's way faster to install a game.
* No VPK means no Henkaku Safe Mode protecting you. And that caused some problems as some people bundled inside MaiDump dump a malware that mount vs0 and os0 as read/write and deleted every file from it, thus bricking the vita\


Oh yeah and at the time there was no vitashell USB support so transferring a vpk was either through ftp, or through QCMA. You rename the .vpk into .mp3, and transfer it as music with QCMA to your PSVita. Then go to ux0:music and rename the .mp3 to .vpk and install.

The advantage of using a decrypted game came down to using plugins. HENkaku had limited support for plugins in ux0:plugins which allows loading user plugins inside decrypted apps. The main use was the amphetamine plugin which allows you to select the CPU and GPU clock speed while playing a game and also the RinCheat plugin.

Fortunately, the next release will bring us a step further to the CFW experience on the vita, and it's the release of Taikaku which is a framework that allows devs to create plugins. Known today as TaiHEN. It was now possible to hook and patch on the kernel and user space. Also fun fact, TaiHEN is based on substitute which is a framework used in the iOS jailbreak scene to load tweaks (plugins) on the system. (Additionally, we were now able to open uncompressed FSELF).\
It was released as beta so we had two options. Either we load HENkaku or taiHENkaku. When it was stable enough it was merged with HENkaku.

We had a few plugins released shortly afterward like f.lux, and TheFloW updated vitashell to support USB mounting which was awesome at the day. No more renaming vpk to mp3 trick !

And the reason that still let some people on 3.18 was finally removed as TheFloW also releases adrenaline (which is very very similar to TN-V by Total\_Noob mmmmmmmmmmmmmmmmmmh) And we now had a ePSPCFW on 3.60. The installation was kind of not as convenient as today where you just need to install a vpk, back then you had to have a PSP game (You could use the Celeste blue method of ePSP Bubble installer to have a 3.5MB PSP game you can use for either Adrenaline or ARK) installed on your vita, install the adrenaline plugin in the config.txt with the TITLE ID of the PSP game you have and download manually the 661.PBP and put it inside the adrenaline folder.\
Well, there was an Adrenaline easy installer app made anyway.&#x20;



## 2017 The arrival of Enso

Having HENkaku was a dream come true, and we thought that we had stagnated after all those releases. Sony patching the HENkaku exploit with 3.61 (webkit) and 3.63/5 (kernel exploit) and no exploit in the horizon we were already aware of how hard it would be to have another HENkaku so we valued 3.60 a lot. But molecule team impressed us again with the announcement of Enso !. We could finally have a permanent CFW with Enso + HENkaku + taiHEN !\


{% embed url="https://youtu.be/KmZeDn5hpos" %}
Enso Xana edition
{% endembed %}



It was such a birthday gift for us as it was released the july 2017, same day as Henkaku, and I remember that I was waiting all day night then doozed off for like 3 hours and my body woke me up automatically 5 min after enso was released at 3 am. I tested immediately the program but refused to install as I had a DEX mod on my vita. I reinstalled the 3.60 firmware and could finally profit from enso on the vita !

Alongside the release of Enso we had another dream come true : MicroSD adapter for the PSVita ! Finally, no more me being stuck with my 8GB memory card and having to deal with QCMA every week to change games. First the PSVSD by Yfanlu and then the SD2Vita by xyz. You can find more information in the SD2VITA History article I made below.

With such progress, we totally broke through the limits of the PSVita and began to dream for other innovations like with this [Wololo post](https://wololo.net/2017/08/30/whats-next-ps-vita-scene/) which represents the mindset of every user back then.

![Oh you don't say?](<.gitbook/assets/image (18).png>)





Piracy was blooming with vitamin and MaiDump, but TheFloW released a surprise that changed the piracy side of the Vita : Nonpdrm ! No more vpk or game folder with maidump, no more risk of having malware inside ! 100% legit game dump untouched (apart the eboot for the fake license) still encrypted ! It also fix an issue we had with decrypted game dump : the ability to install updates from liverea ! (granted the update doesn't require a fw higher than 3.60.&#x20;

Motoharu also provided another way of having a completely legit backup dump with psgamesd which creates a 1:1 dump of the cartridge and allows playing it by creating a virtual cartridge on the vita. This format is considered as the best one if we goes into the preservation of the Vita library but it won't meet its success as nonpdrm was more practical.

Motoharu will also release a set of tool on pc like psfpsvtools which allows to decrypt any PSF encrypted vita file directly from the PC. No need for vitashell now.

As for better 3D homebrew support, we had an amazing exploit by VitaHex, who graced us with many homebrew like Switch UI which replicate the menu of the switch for the vita (which can be launched at boot directly with enso without seeing the live area). He released zombiebound, a zombie shooter in 3D made in lua and it was the first real 3D homebrew for the PSVita.

&#x20;What about streaming the PSVita screen on the PC? Well we have Vita2PC by rinnegatamante which allows to stream the PSVita through wifi, and xerpi teased his usb solution. On the other hand we had moonlight and PC-Link to stream the PC screen on the PSVita.

2017 is the year where activation is a big issue. Sony did something on 3.60 (intentional or not I don't know since it was reverted in 2019) which prevented users from activating their PSVita. Worse if you connect to the PSN the activation file will get deleted automatically in most cases ! (Fortunately, I had a backup of my activation file so I wasn't screwed but a lot of users were). It might not sound like a big deal for you but back then activation meant a lot. We needed it in order to use adrenaline. No activation = no base PSP game = no adrenaline. There was a first solution called MLTactivator (don't use it) which replace your account with an activated account on the vita but had a downside. 1 It's not your account anymore 2 You can't go to PSN.\
The second solution will be brought by Celeste-Blue with ReStore and ReNpDRM. It was first deemed impossible by Yfanlu without a f00d exploit (f00d is the security processor of the PSVita) but he managed to bring back the activation on 3.60 ! The purpose is simple : it constantly refreshes for activation so even if sony automatically removes the activation it gets back. But how does it get the activation file if we can't activate our PSVita the normal way?\


The problem was that the success of the operation was a hit and miss, a lot of users complained that it didn't work, others stated we needed restore v1 with renpdrm v5 in order for it to work. Other had stated that sony automatically removes restore from ur0:tai (I'm sure it's bullshit). So we needed another reliable solution.



The end of the year saw the release of the 3.67 firmware which fix the KRACK vulnerability on the wifi firmware as well as patching a vulnerability that used in chain with other vulnerabilities allows for persistence.

## 2018 VitaGL and 3.65/8 now hacked

2018 started with a huge showcase : VitaGL was announced which would open the door to 3D homebrew and ports using OpenGL on the PSVita ! No more gxm learning to develop something in 3D ! At the same time, Vita3K was announced and showcased homebrew using VitaGL running on it. The 3D era of the PSVita has begun !\
VitaQuake 2.5 was released and it was the first hardware-accelerated homebrew on the vita using OpenGL. We had vitaXash3D next, a port of Half-Life. The saga continues and we saw more ports using OpenGL on the PSVita increasing its library.\
\
Enso source code was released and TheFloW built the 3.65 enso installer which allows for 3.60 users to go to 3.65 enso ! It was the first time that we could hack another firmware after 2 years and while it does not involve another vulnerability, it was kind of dangerous as it relies on enso to load the hack. It "update" the PSVita while on and patch the bootloader with enso hack then reboot to finally lend on 3.65 enso (so that means 3.61+ users couldn't hack the 3.65 firmware). But if for some reason enso doesn't work or is removed through restoring the system or whatever could remove it, then you end up in stock 3.65 with no way of hacking back. This has left most people questioning themselves if they should do the jump to either profit more game support with 3.65 as well as activation fixed but with a risk of losing the hack permanently or staying on 3.60. Fortunately, that question was quickly gone with people backporting 3.65 games and updates to 3.60 with MaiDump and Vitamin.

5 months later, with the release of 3.68, TheFloW confirms that it hasn't patched his vulnerability and decided shortly after, the 1 July, to release h-encore. We finally had another exploit 2 years after HENkaku !

Still many people stayed on 3.60 masterace because 3.65 needed many software and plugins to be updated to work on 3.65.

Another issue with the 3.65 firmware is that Sony patched loading decrypted content from ux0:patch which blocked the modding of games. Fortunately, Dots-TB released repatch which acts as a decrypted patch folder and allows modding games back again.&#x20;

People again backported games to 3.60 but the MaiDump and Vpk format was not great to deal with and while nonpdrm was superior, we had no choice but to use them. That is until the #Letmaidie project arrived.\
Team Faps (huh?) released FAGdec (huh huh?) which allows to decrypt user/kernel and games modules generating compatibility packs .ppk used to load 3.68 games on 3.60 using either legit cartridge and digital games or nonpdrm dump.

3.69 (nice) was released and patched the h-encore exploits, and xerpi has released his USB streaming plugin while customization reaches a new level with font changing and custom boot splash. The Vita scene is blooming and another breakthrough will be made : Overclocking

We can already overclock our vita with PSV Shell but it's just changing the base speed to its highest speed. Now we could go further beyond and Lolicon was released (Don't arrest me I swear I'm not like that) and we could overclock the CPU speed to 500Mhz which brings a lot of improvement for some games like Killzone which eliminate any frame drop and also helps with emulators performances.&#x20;

More games were added to the PSVita library with the release of Gaymaker (Man 2018 is really the horniest year for the PSVita) which allows porting games made using Game Maker to the PSVita without needing the source code.&#x20;

Day after day, the PSVita capacities were improved and 2018 is a major turn point in PSVita history.  Can we go further yet?



## 2019 PSVita security defeated, scam everywhere

2019 is probably the year where the PSVita security was gone forever, in 2012 what was once estimated as the toughest security system made in place for a mobile device is now completely defeated in 2019. \
F00D is a crypto-security processor which handles most of the PSVita cryptography tasks including storing and handling of the most secure keys. The article from [Wololo](https://wololo.net/2018/12/30/psvita-hacking-35c3-summary-of-talk-f00d-bootloader-key-revealed-and-team-molecule-releases-various-decryption-tools-now-the-psvitas-security-is-effectively-blown-wide-open/) covers well the matter. But it's kind of funny that the key found by the most absurd way by xyz (bruteforcing a AES-128 key, you must be either a genius or an idiot to attempt that) is an amazon product :joy:. (For those who didn't understand the joke the key is AAAAAAAAAAAAAAAA, which is as dumb as using 12345 as a password for your account).\
\
With F00D saw the release of reF00D which allows the users to play 3.69 games on 3.60 without needing compatibility packs or people going to 3.69 to decrypt the game.

This also allowed downgrading with the release of Modoru, now we can safely go back from 3.68 to a firmware that has enso.

Trinity was released and the latest up-to-date hack for the Vita was what allowed the PSVita to be hacked in the first place : epsp. This exploit is a real tribute to the PSVita hacking legacy as it was the end goal of early hackers to use epsp exploit into a native hack and TheFlow managed to do it at last. TheFloW also released h-encore² which improves the reliability of the exploit for 3.63/8\
\
F00D control also allows to remove the blacklist made by sony and thus allowing us to bring back the PSM for dev and Unity for Dev apps used back then in rejuvenate ! This means that unity homebrew was possible on the PSVita !

Following the wave of popularity that the PSVita is going through, a homebrew contest and an indieGoGo campaign have been done. The first one is called VitaGamJam. It's a Game contest made for the vita by an unknown person from Twitter who appeared from nowhere. The organization was very very sketchy with a Twitter poll voting system and a 500$ price for the winner. After some investigation, it turned out that the whole thing was a scam as the author of the contest was disappointed by the entries and decided to submit his own project and make it win to save his money. The whole explanation about that scam can be found [here.](https://wololo.net/2019/05/22/vitajam2019-explained-opinion/)

The second scam is the VitaDock. The original goal was to provide the community with a device that act as a dock which like the Nintendo Switch will stream the PSVita screen to the TV and thus act like a PSTV if used with a ds4 plugin. The campaign collected around 17,700$ in total. xCorra was working on the project while sending some showcases about his progression. He also acted as a helper alongside me in the Henkaku discord and began to earn people's trust increasing his indieGoGo funding. While he came close to me and shared some of his "private life" information like how his wife was in the hospital and it was kind of hard for him lately. He vanished shortly after from the internet and was nowhere to be found until later where xSis reddit account apologized about the vitadock and claimed it will refund the people who invested on it (Spoiler : no). I first thought that it was because of depression and the situation with his wife but he came&#x20;

