##  ##

<div align="center">
  
![image](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/image/Readme.png)
  
</div>

##  ##


<div align="center">
  
# **Purge Adaptive Klipper** #
  
</div>

##  ##

Ce projet, appelé **KAMP** (KlipperAdaptiveMeshingPurging), a été créé pour simplifier l'utilisation d'une purge adaptative sur Klipper. 
<br><br>

La Purge adaptative permet d'utiliser les valeurs d'un fichier Gcode pour définir l'emplacement de la purge en fonction de la taille de votre print.
<br><br>

# **Pourquoi utiliser la Purge Adapative** #
<br>
L'avantage de cette purge et de ne pas avoir une ligne toujours au même endroit sur votre Bed et même de pouvoir ce passer de la jupe.
<br>
Cela permet aussi de gagner du temps ( peu mais c'est toujours ça) en évitant des déplacements sur tout votre plateau.

# **Comment fonctionne la purge adaptative** #
<br>

Grâce au travail de [kageurufu](https://github.com/kageurufu) sur [[exclude_object]](https://github.com/kageurufu/preprocess_cancellation) dans le firmware Klipper, il est possible d'extraire la taille d'un objet tranché ce qui nous permet de connaitre la position de votre print et d'adapter la position de votre purge.
<br>
En analysant plusieurs objets dans le fichier Gcode, la purge (logo ou ligne) peut s'adapter à n'importe quel objets.

<br><br>

Aller, nous allons voir comment [Installer ceci](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/Installation.md)
