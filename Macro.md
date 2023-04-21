##  ##

<div align="center">
  
# **Macro Start Print** #
  
</div>

##  ##

Avant d'utiliser des macros de KAMP lors de l'utilisation de la méthode gérée moonraker, vous devez définir les paramètres des macros avant qu'elles ne soient appelées.
<br>
Sinon elles n'utiliseront que les paramètres par défaut. 
<br>
Vous ne devriez avoir à modifier votre PRINT_START qu'une ou deux fois jusqu'à ce que les paramètres soient définis comme vous les aimez,
<br>
puis vous pouvez les laisser seuls.
<br>
Un exemple est fourni au bas de cette section pour vous montrer comment procéder.
<br>
<br>

## ## 

# **Inclure les macros dans le Start_Print** #

<br>
    
## ##
1.Pour la purge adaptative en forme de logo Voron :

```
SETUP_VORON_PURGE [parameters]
```

<br>

## ##
2.Pour une purge adaptative sous forme de ligne simple :

```
SETUP_LINE_PURGE [parameters]
```

<br>

## ##

**Exemples de START_PRINT:**

<br>

```
[gcode_macro PRINT_START]
gcode:
    SETUP_KAMP_MESHING DISPLAY_PARAMETERS=1 LED_ENABLE=1 FUZZ_ENABLE=1 # PURGE ADAPTATIVE
    SETUP_VORON_PURGE DISPLAY_PARAMETERS=1 ADAPTIVE_ENABLE=1           # PURGE ADAPTATIVE
    .
    M140 S{BED_TEMP}
    M190 S{BED_TEMP}
    M109 S{EXTRUDER_TEMP}
    .
    .
    G28     
    G90     
    M117    
    G92 E0  
    G1 Z10.0 F3000  
    .
    VORON_PURGE     # PURGE ADAPTATIVE 
    .
    G1 Z1.0 F3000   
    M220 S100       
```

<br>

## ## 
<br>

Voici une explication de chacun des paramètres:
<br><br>
-**DISPLAY_PARAMETERS=1:** Ce paramètre permet d'afficher les paramètres de la fonction de maillage de lit sur l'écran de l'imprimante 3D.

-**LED_ENABLE=1:** Ce paramètre permet d'allumer une LED sur l'imprimante 3D lors de la réalisation de la fonction de maillage de lit.

-**FUZZ_ENABLE=1:** Ce paramètre permet de réaliser une fonction de "fuzzing" (approximation) pour compenser les erreurs de mesure et améliorer la précision du maillage de lit.
<br>
<br>

## ##

Il est **très important** que les **SETUP_macros** soient appelées avant la macro réelle **Voron_Purge**, sinon les valeurs par défaut sont utilisées.
<br>

Nous allons voir les [paramètres](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/Param%C3%A8tres.md) à régler pour notre purge.
