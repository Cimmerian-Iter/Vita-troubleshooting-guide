---
description: Le multi des jeux Vita vivront éternellement yeahhhhhhhh
---

# Comment utiliser Xlink

Grâce à Xlink, nous pouvons maintenant sauver des jeux tel que Freedom Wars ou Soul Sacrifice Delta dont le multi-joueurs constituait une grande partie de l'intérêt de jouer à ces jeux. Grâce au mode Ad-Hoc, le PC va se connecter au réseau Ad-Hoc de la Vita, et faire une sorte de tunnel qui permettra aux Vita du monde entier de se connecter au réseau Ad-Hoc de la Vita.  C'est le même principe que Ad-Hoc Party sur PS3 pour la PSP. Le tout GRATUITEMENT\




## Comment j'installe Xlink?

Tout d'abord vous avez besoin de ces élements :&#x20;

1. Une PSVita (non hacké ou hacké peu importe, les deux marchent)
2. Un PC (Sous Windows, Linux Ou même MacOs)
3. Un compte Xlink
4. Une carte wifi compatible ou un adaptateur wifi compatible (Généralement votre carte wifi de base devrait marcher, si dans la suite du tutoriel vous n'arrivez pas a connecter votre Vita dans xlink, c'est qu'il faut acheter une carte wifi. Voici une list des carte wifi recommandé : [lien](https://www.teamxlink.co.uk/wiki/PSP\_WiFi\_Adapters) )
5. Un moyen d'avoir Internet sur votre PC sans votre carte wifi (Comme on va utiliser la carte wifi pour se connecter au réseau de la Vita, il nous faut soit une connexion Ethernet, une deuxième carte wifi ou un partage de connexion de votre téléphone via USB pour que l'ordinateur puisse se connecter à Internet.)

## Obtenir un compte Xlink&#x20;

C'est très simple, allez dans le site puis créez un compte Xlink kai\
[https://www.teamxlink.co.uk/u/register](https://www.teamxlink.co.uk/u/register)\
\
Gardez dans un coin de votre tête votre gamer tag et votre mot de passe, nous on aurons besoin de ceci ensuite.

## Installer Xlink kai sur votre PC

Tout d'abords nous aurons besoin d'installer un module très important pour la gestion de la communication réseau. \
\
Pour un PC Windows

1. Obtenez ncap depuis ce [lien](https://nmap.org/npcap/dist/npcap-1.31.exe)&#x20;
2. Installez le (Laissez les case coché comme elles sont, si il veut désinstaller wincap alors faites le)
3. Obtenez Xlink kai depuis ce [lien](https://www.teamxlink.co.uk/go?c=download)
4. Installez Xlink kai
5. Lancez Xlink kai
6. Connectez vous \
   ![](<../.gitbook/assets/image (21).png>)

Vous voila donc dans le menu principal de Xlink kai. Veuillez laisser cette fenêtre ouverte, nous allons maintenant essayer de connecter votre Vita avec le PC\
\
**Pour un PC linux ou Mac**

Les instructions pour ces systèmes d'exploitations sont indiqué dans le wiki pour [Linux](https://www.teamxlink.co.uk/wiki/Installing\_on\_Raspberry\_Pi) et [MacOs](https://www.teamxlink.co.uk/wiki/Installing\_on\_macOS)

## Connecter la PSVita au PC

La partie la plus importante, et elle n'est pas plus compliqué.



* Téléchargez [XLHA](https://github.com/codedwrench/xlinkhandheldassistant/releases/tag/REL\_1\_2), un outil qui s'occupera de gérer la connexion de la PSVita vers le PC (Si vous avez un PC Windows, téléchargez le zip Windows, puis extrayez le .exe de ce zip quelque part)
* Lancez XLHA (Au cas ou, vous avez un readme qui vous détaille en anglais comment lancer XLHA selon votre système d'exploitation)\
  \
  Vous vous retrouvez face à une fenêtre de ce type :&#x20;



![Ca fait très hackeur tout ça](<../.gitbook/assets/image (17).png>)

* Naviguez avec les touches directionnel, sélectionnez Vita Device, puis appuyez sur entrée pour le cocher
* Naviguez vers NEXT puis appuyez sur Entrée
* Au prochain écran, naviguez vers Automatically Connect to PSVita networks et appuyez sur entrée pour le cocher (Cela permettra au programme de scanner automatiquement et de se connecter automatiquement à un réseau PSVita)
* Dans Use the following Network, sélectionnez la carte wifi qui sera utilisé pour la connexion avec la PSVita. Si vous ne savez pas, ouvrez le panneau de configuration, puis allez dans "Réseau et Internet", puis "Centre Réseau et partage" puis "Modifier les paramètres de la carte" et vous aurez une liste des carte wifi sur votre PC ainsi que leurs nom.

![J'utilise un adaptateur USB TP-Link pour la Vita donc son nom est Wi-Fi 2](<../.gitbook/assets/image (22).png>)

* Changez la valeur de "Reconnect after network has been inactive for \<seconds>" à 1 (C'est le temps nécessaire au programme pour tenter de se reconnecter à un réseau PSVita)

![Voila à quoi doit ressembler votre écran](<../.gitbook/assets/image (20).png>)

* Appuyez sur Next, puis encore sur Next (ne changez rien dans les ports et adresse IP)

Vous arrivez donc sur cet écran.&#x20;

![Oh le beau champignon](<../.gitbook/assets/image (16).png>)

Il ne vous reste plus qu'a faire Start Engine, et le programme va chercher automatiquement un réseau PSVita



![](<../.gitbook/assets/image (26).png>)\
