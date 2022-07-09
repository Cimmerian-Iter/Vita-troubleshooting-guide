---
description: Le multi des jeux Vita vivront éternellement yeahhhhhhhh
---

# Comment utiliser Xlink

Grâce à Xlink, nous pouvons maintenant sauver des jeux tel que Freedom Wars ou Soul Sacrifice Delta dont le multi-joueurs constituait une grande partie de l'intérêt de jouer à ces jeux. Grâce au mode Ad-Hoc, le PC va se connecter au réseau Ad-Hoc de la Vita, et faire une sorte de tunnel qui permettra aux Vita du monde entier de se connecter au réseau Ad-Hoc de la Vita.  C'est le même principe que Ad-Hoc Party sur PS3 pour la PSP. Le tout GRATUITEMENT

\


![Retour vers l'époque Windows 7](<../.gitbook/assets/image (26) (1).png>)

{% hint style="info" %}
Comme il s'agit d'une connexion Ad-Hoc, aucune données sensible n'est transmise comme votre id PlayStation Network. Les serveurs Xlink ne gardent pas de traces de vos parties, ils s'occupent uniquement de vous relier entre les PSVita du monde, la connexion est du P2P entres les ordinateurs. Donc si vous avez des craintes par rapport à votre privé et bien il n'y à rien à craindre.
{% endhint %}



## Comment j'installe Xlink?

Tout d'abord vous avez besoin de ces élements :&#x20;

1. Une PSVita (non hacké ou hacké peu importe, les deux marchent)
2. Un PC (Sous Windows, Linux Ou même MacOs)
3. Un compte Xlink
4. Une carte wifi compatible ou un adaptateur wifi compatible (Généralement votre carte wifi de base devrait marcher, si dans la suite du tutoriel vous n'arrivez pas a connecter votre Vita dans xlink, c'est qu'il faut acheter une carte wifi. Voici une list des carte wifi recommandé : [lien](https://www.teamxlink.co.uk/wiki/PSP\_WiFi\_Adapters) )
5. Un moyen d'avoir Internet sur votre PC sans votre carte wifi (Comme on va utiliser la carte wifi pour se connecter au réseau de la Vita, il nous faut soit une connexion Ethernet, une deuxième carte wifi ou un partage de connexion de votre téléphone via USB pour que l'ordinateur puisse se connecter à Internet.)

{% hint style="info" %}
Pour le 5e point, je vous conseille vivement de forcer votre PC à utiliser la carte wifi/Ethernet/Partage de connection, pour cela vous pouvez deconnecter la carte wifi (que vous utiliserez pour la connecter à votre PSVita) du réseau auquel elle est connecté que vous utiliserez.  Votre PC va donc utiliser l'autre moyen de se connecter à internet.
{% endhint %}

## Obtenir un compte Xlink&#x20;

C'est très simple, allez dans le site puis créez un compte Xlink kai\
[https://www.teamxlink.co.uk/u/register](https://www.teamxlink.co.uk/u/register)\
\
Gardez dans un coin de votre tête votre gamer tag et votre mot de passe, nous on aurons besoin de ceci ensuite.



## Installer Xlink kai sur votre PC

Tout d'abords nous aurons besoin d'installer un module très important pour la gestion de la communication réseau. \
\
Pour un PC Windows

1. Obtenez ncap depuis ce [lien](https://npcap.com/dist/npcap-1.60.exe)&#x20;
2. Installez le (Laissez les case coché comme elles sont, si il veut désinstaller wincap alors faites le)
3. Obtenez Xlink kai depuis ce [lien](https://www.teamxlink.co.uk/go?c=download)
4. Installez Xlink kai
5. Lancez Xlink kai
6. Connectez vous \


![uk? Les rosbeef ont fait ce truc?](<../.gitbook/assets/image (21) (1) (1) (1).png>)

Vous voila donc dans le menu principal de Xlink kai. Veuillez laisser cette fenêtre ouverte, nous allons maintenant essayer de connecter votre Vita avec le PC\
\
**Pour un PC linux ou Mac**

Les instructions pour ces systèmes d'exploitations sont indiqué dans le wiki pour [Linux](https://www.teamxlink.co.uk/wiki/Installing\_on\_Raspberry\_Pi) et [MacOs](https://www.teamxlink.co.uk/wiki/Installing\_on\_macOS)

## Connecter la PSVita au PC

La partie la plus importante, et elle n'est pas plus compliqué.



* Lancer un Jeu PSVita qui utilise le Ad-Hoc, et activez le Ad-Hoc dans ce jeu.\

* Téléchargez [XLHA](https://github.com/codedwrench/xlinkhandheldassistant/releases/tag/REL\_1\_2), un outil qui s'occupera de gérer la connexion de la PSVita vers le PC (Si vous avez un PC Windows, téléchargez le zip Windows, puis extrayez le dossier de ce zip quelque part)
* Lancez Xlink Handlheld Assistant (Au cas ou, vous avez un readme qui vous détaille en anglais comment lancer XLHA selon votre système d'exploitation)\
  \
  Vous vous retrouvez face à une fenêtre de ce type :&#x20;

![Ca fait très hackeur tout ça](<../.gitbook/assets/image (17).png>)

* Naviguez avec les touches directionnel, sélectionnez Vita Device, puis appuyez sur entrée pour le cocher
* Naviguez vers NEXT puis appuyez sur Entrée
* Au prochain écran, naviguez vers Automatically Connect to PSVita networks et appuyez sur entrée pour le cocher (Cela permettra au programme de scanner automatiquement et de se connecter automatiquement à un réseau PSVita)
* Dans Use the following Network, sélectionnez la carte wifi qui sera utilisé pour la connexion avec la PSVita. Si vous ne savez pas, ouvrez le panneau de configuration, puis allez dans "Réseau et Internet", puis "Centre Réseau et partage" puis "Modifier les paramètres de la carte" et vous aurez une liste des carte wifi sur votre PC ainsi que leurs nom.

![J'utilise un adaptateur USB TP-Link pour la PSVita donc son nom est Wi-Fi 2](<../.gitbook/assets/image (22) (1) (1) (1).png>)

* Changez la valeur de "Reconnect after network has been inactive for \<seconds>" à 1 (C'est le temps nécessaire au programme pour tenter de se reconnecter à un réseau PSVita)

![Voila à quoi doit ressembler votre écran](<../.gitbook/assets/image (20) (1) (1) (1).png>)

* Appuyez sur Next, puis encore sur Next (ne changez rien dans les ports et adresse IP)

Vous arrivez donc sur cet écran.&#x20;

![Oh le beau champignon](<../.gitbook/assets/image (16).png>)

Il ne vous reste plus qu'à faire Start Engine, et le programme va chercher automatiquement un réseau PSVita



![Ah non c'est une libellule en fait](<../.gitbook/assets/image (26) (1) (1).png>)

Voila, votre PSVita est bien connecté à votre PC comme vous pouvez le voir en haut à gauche avec le magnifique SCE (Sony Computer Entertainment)



{% hint style="info" %}
Si votre PC n'arrive pas à detecter de réseau PSVita, vérifier que votre PSVita à bien lancé une connexion Ad-Hoc. Si cela ne marche toujours pas, il faudra changer de carte wifi.
{% endhint %}

## Rejoindre un lobby&#x20;

Se connecter c'est bien, jouer c'est mieux. Maintenant retournez dans votre fenêtre Xlink kai que nous avions ouvert avant. Si vous appuyez sur le bouton Metrics vous devriez voir votre PSVita connecté&#x20;

![2 consoles pour le prix d'une](<../.gitbook/assets/image (21) (1) (1).png>)

&#x20;

{% hint style="info" %}
Si vous ne voyez pas votre PSVita, essayer de rejoindre un lobby pour que la PSVita soit reconnu. Si votre PSVita n'est toujours pas reconnu malgrès que XLHA soit connecté au réseau Ad-Hoc de la PSVita, votre carte wifi est incompatible. Vous allez devoir en acheter une qui soit compatible.
{% endhint %}

\
Appuyez sur Game Arenas pour avoir la listes des lobby selon les consoles.

![Des gens qui jouent a Black ops Cold War??? Alors que les serveurs marchent? Ca doit être des gens qui veulent pas payer le PS+](<../.gitbook/assets/image (28) (1) (1).png>)

Choisissez PSVita, puis selectionnez la categorie de jeux qui concerne le jeu auquel vous voulez jouer. Puis choissisez votre jeu dans la liste.

Une fois choisi, vous êtes dans un lobby public.&#x20;

![Je me sens si seul..... Si seulement adopteunami.com existait](<../.gitbook/assets/image (19) (1).png>)

Au centre vous avez le chat général du lobby, à droite la liste des utilisateurs connecté au lobby ainsi que leurs ping qui s'affichera via une barre coloré en dessous de leurs nom.

Mais comment ça marche maintenant? Et bien comme vous êtes dans un même lobby, vous pouvez soit host une partie Ad-Hoc sur votre vita du jeu de votre choix, ou rejoindre une partie avec votre jeu. Les PSVita des autres utilisateurs s'afficheront sur votre vita comme si elles étaient à 30cm de vous. C'est du Ad-Hoc, le principe reste le même. Maintenant amusez vous !





{% hint style="info" %}
Pour des jeux commes Freedom Wars, qui n'ont pas d'options créer, ou rejoindre une partie et qui s'occupe automatiquement de chercher d'abord si il y a une partie avant de créer soit même sa partie, le processus de connexion peut être plus fastidieux. En effet Freedom Wars prend 3 seconde pour chercher une partie ce qui peut être court; Je vous conseille de proceder comme cela :  \
1 Rejoignez avec vos amis un lobby Freedom Wars\
2 Lancer XLHA sur votre PC\
3 Selectionner la chambre ou vous allez tous vous rejoindre sur Freedom Wars (room 1 par exempe)

4 XLHA devrait se connecter immediatement à la PSVita et avec un peu de chance reussira à connecter la PSVita aux autres PSVita et ainsi créer la partie Ad-Hoc commune\
\
Note : Il se peut que une fois dans le jeu, vous ne voyez pas immédiatement les personnages des autres utilisateurs, c'est normal. Laissez quelque minutes le temps que le jeu finisse de se synchroniser et les personnages des joueurs devraient tous s'afficher.
{% endhint %}

{% hint style="info" %}
Pour Soul Sacrifice Delta, il faut obligatoirement une PSVita hacké, en effet le jeu possède une limite de ping maximum de 30ms, or en utilisant Xlink, le ping est plus élevé. Le jeu va donc forcer la deconnexion. Pour contourner ce problème il faut patcher le jeu. Voici un [tutoriel](https://www.teamxlink.co.uk/wiki/Soul\_Sacrifice\_Delta)
{% endhint %}

{% hint style="info" %}
Si vous voulez faire un lobby privé, appuyé sur le petit crayon à coté de l'étoile. Vous pourrez ensuite créer un lobby protégé par mot de passe.&#x20;
{% endhint %}

