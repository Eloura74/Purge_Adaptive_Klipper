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

Il est **très important** que les **SETUP_macros** soient appelées avant la macro réelle **Voron_Purge**, sinon les valeurs par défaut sont utilisées.
<br>

Nous allons voir les [paramètres](https://github.com/Eloura74/Purge_Adaptive_Klipper/blob/main/Param%C3%A8tres.md) à régler pour notre purge.
