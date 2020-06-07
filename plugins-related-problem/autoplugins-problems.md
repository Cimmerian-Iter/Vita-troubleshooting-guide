# Erreur lors de l'utilisation de Autoplugin :

#### Parfois, l'Autoplugin échoue et nous savons que l'Autoplugin 1 a tendance à corrompre le config.txt \(et récemment l'Autoplugin 2 avait le même soucie, bien que le problème ait été résolu dans la v1.05 à ce jour\) Il est important de savoir comment gérer les plugins. Autoplugin est un excellent homebrew, mais il ne devrait pas remplacer totalement la connaissance des plugins et vous ne pouvez pas vous attendre à ce qu'il soit à toute épreuve. Nous verrons donc comment récupérer d'un mauvais comportement les beugs d'Autoplugin en apprenant comment fonctionnent les réglages.

## Qu'est-ce qu'un plugin ?

Vous l'avez peut-être déjà rencontré dans la scène PSP, les plugins sont des microprogrammes qui s'exécutent en arrière-plan et améliorent votre expérience. Son but peut être divers comme gérer l'overclocking, la modification du livearea ou une fonction native \\(comme la capture d'écran ou le lecteur de musique\\). Ils sont essentiels de nos jours. Ils sont chargés par le framework de TaiHEN grâce à l'effort de la Team Molecule.

Il y a deux types de plugins :

SKPRX : il s'agit de plugins du noyau (kernel), le plus courant de nos jours, il modifie les fonctions générales de votre PSVita. Comme Nonpdrm pour simuler le système de DRM, Yamt-lite pour charge la SD2VITA comme une carte mémoire internet de la PSVita et bien plus encore. Ils ont besoin d'un redémarrage entre l'installation pour fonctionner. \(Ou utiliser le chargeur de plugin de xerpi's "vita_plugin_loader"\)

SUPRX : ce sont des plugins utilisateurs, nous pouvons diviser en deux groupes : ceux qui modifient le livearea (menu de la PSVita) \\(\\*main\\), et ceux qui modifient les jeux/applications \\(\\*TOUT\\). Pour savoir quelle catégorie le plugin appartient, vous devez soit savoir ce qu'il fait, ou lisez simplement la description depuis son github \(ils vous disent souvent si vous avez besoin de l'installer sous \*main ou \*ALL\)  
Ils n'ont pas besoin d'un redémarrage pour être chargés, le rechargement du fichier config.tx de taiHEN dans les Paramètres de HENkaku devrait faire l'affaire.



## Comment installer un plugin ?

Cette partie n'est pas vraiment difficile. C'est assez facile en fait. Il vous suffit d'écrire juste quelques lignes.

Pour installer des plugins, vous devez faire 2 choses :

### Placez les plugins dans le dossier ur0:tai \(ou ux0:tai si vous voulez utiliser ux0\)

Les plugins se placent dans le dossier tai où se trouve le fichier config.txt. Il peut y avoir une exception telle que vitacheat.suprx où il doit être dans son propre dossier vitacheat dans ux0

### Écrivez le chemin d'accès au plugin dans le fichier config.txt

Le chemin d'accès est l'emplacement du fichier. Si le plugin est situé dans ur0:tai, alors le chemin est : ur0:tai/name.skprx  
Vous devez écrire le chemin dans le config.txt sous la catégorie du plugin.  
KERNEL : skprx  
MAIN : modification du livearea  
TOUS : modifications des applications

Voici un exemple. Imaginons que j'ai un répertoire tai en ur0 qui contient:  
KERNEL : storagemgr.skprx, lolicon.skprx, nonpdrm.skprx  
MAIN : shellbat, download enabler  
TOUS : vitacheat \(skprx est en ur0:tai/, suprx en ux0:vitacheat/\)

```bash
*KERNEL
ur0:tai/storagemgr.skprx
ur0:tai/lolicon.skprx
ur0:tai/nonpdrm.skprx
ur0:tai/vitacheat.skprx

*main #main needs to be in lowercase
ur0:tai/shellbat.suprx
ur0:tai/download_enabler.suprx

*ALL
ux0:vitacheat/vitacheat.suprx

```


Vous pouvez également spécifier quelle application chargera le plugin, par exemple si vous voulez activer vitacheat uniquement dans certains jeux, vous devez écrire le chemin du fichier sous le nom de code de l'application. Pour connaître le nom de code de l'application, soit vous cherchez avec Vitashell le nom de code de l'application dans ux0:app \(souvent facile à deviner avec les noms), soit vous cherchez sur Google le nom de code du jeu que vous voulez. Pour les utilisateurs expérimentés, vous pouvez facilement connaître le nom de code d'une application en affichant les informations de l'application sur le livearea.  
De plus, vous pouvez spécifier quelle application ne chargera pas le plugin. Il peut être utile, par exemple, lorsqu'un réglage de l'overclock fait planté Adrénaline. Pour cela, vous devez ajouter un "!" avant le nom de code qui arrête l'exécution du plugin lors de l'ouverture de l'application spécifiée.

Voici un exemple, je veux activer Vitacheat dans le jeu Killzone seulement, et je ne veux pas charger le plugin lolicon dans Adrénaline.


```text
*PCSF00243
ux0:vitacheat/vitacheat.suprx

*!PSPEMUCFW
ur0:tai/lolicon.skprx
```

### N.B :

1. Si vous utilisez une SD2VITA, ux0:tai NE DOIT PAS exister. Supprimez-le et mettez tous les plugins dans ur0:tai. 0/> Le plugin SD2VITA que vous utilisez doit toujours être en haut de \*KERNEL, sinon les autres plugins ne fonctionneront pas correctement. La raison pour laquelle vous devrez le faire est que lorsque vous chargez le plugin SD2VITA à partir de ux0, il échange le répertoire ux0 contre celui de votre SD2VITA. Le problème est qu'il essaie d'accéder à nouveau au plugin, mais comme ux0 a été échangé, il ne peut pas trouver le plugin.

2. Sachez que les plugins ont un impact, si vous chargez trop de plugins, vous pouvez vous attendre à quelques ralentissements ou, dans le pire des cas, à un bootloop. C'est particulièrement vrai si vous avez tendance à avoir plus de 10 plugins, ou si vous chargez le plugin xerpi usb screenshare \(qui est lourd) avec beaucoup de plugins.

Essayez de charger uniquement les plugins nécessaires. Si votre PSVita boucle au démarrage, vous pouvez, pour les utilisateurs d'enso, tenir la touche L lors du démarrage pour éviter de charger des plugins, ou pour les 3.61+, ouvrir h-encore et faire un reset taiHEN.

Les utilisateurs d'Enso (3.65) peuvent avoir à formater leur carte mémoire si le fichier id.dat est toujours dans la carte mémoire (le fichier qui indique le firmware et le compte PSN de l'utilisateur) et comme nous déchargeons les plugins, nous désactivons également le spoof du firmware, donc quand la PSVita lira ce fichier, elle vous demandera de mettre à jour la console afin de l'utiliser ou de le formater. Vous n'aurez d'autre choix que de formater ou de mettre à jour vers 3.73 \(à ce moment\). Les utilisateurs des versions 3.60 peuvent toujours réinitialiser HENkaku via l'exploit WebKit sans formater la carte mémoire \(vous démarrerez sur un livearea vierge\) et déconnecter la carte mémoire via les Paramètres de HENkaku, mais pour les utilisateurs des versions 3.65, puisque vous n'avez pas accès à la carte mémoire, vous ne pourrez pas réinitialiser taiHEN. \(Une autre raison pour laquelle je recommande à tout le monde de dowwgrader jusqu'en 3.60\)
