---
description: Wait, people still have hope?
---

# Borderlands 2

Borderlands 2 is a legendary game on the PSVita, not because it's an awesome game or something, but because the port was horribly optimised. Since the franchise was so popular, people began attempting to revive it with some tweaks to make it playable. Reddit user \(u/MODman01\) claims to have found a ‘golden’ setup \(a mix between best graphics and performance\). They have shared their setup:

* Use the latest version of Borderlands 2 \(1.09 as of now, and forever I suppose\) 
* Use nonpdrm, not maidump or .vpk \(Legit bought game should work too since they aren't different from nonpdrm format apart from a legit license\)
* Overclock to 500MHz
* Use VitaGrafix to set the Framebuffer to: 640x368.
* And the last thing is installing the [Patch](https://mega.nz/file/ySByCKYJ#Z_nHwp6NCjXN6HB-OT1qqaB-pot3wbn9kGDCdot8764),  \(Installation instructions are the folder directory and names\)



Some comments from the OP:

> So, after all the testing I have done for this game I found out some interesting stuff.
>
> The only way to make the game run better \(FPS wise\) is to overclock and reduce the screen res to: 640x368.
>
> No matter how low the texture res or the object spawn range is, it doesn’t affect the performance not even by 1 fps.
>
> For the record, this is everything that you can change in the game files:

```text
MaxSmoothedFrameRate=
ONLY NEED TO CHANGE THE FIRST ONE
DOESNT EFFECT PERFORMANCE
-----------------------------------------------------------------------------------
ViewDistanceConsoleScale=
DOESNT EFFECT PERFORMANCE
-----------------------------------------------------------------------------------
DefaultPostProcessName=
WIHOUT OUTLINE: WillowEngineMaterials.CinematicScenePostProcess
WITH OUTLINE: WillowEngineMaterials.WillowScenePostProcess
DOESNT EFFECT PERFORMANCE
BUG: THE DUST, MOUNTAINS
-----------------------------------------------------------------------------------
TEXTUREGROUP_World=
STOCK: 1024
ONLY NEED TO CHANGE THE FIRST ONE
DOESNT EFFECT PERFORMANCE
-----------------------------------------------------------------------------------
```

And that's it. If you have any questions or suggestions, you can contact u/MODman01 on Reddit.

