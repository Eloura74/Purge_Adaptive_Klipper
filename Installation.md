
##  ##


<div align="center">
  
# **Installation** #
  
</div>

##  ##
<br>

Vous devez tout d'abord définir **exclude_object** dans votre fichier **printer.cfg**.
<br>
Assurez-vous d'avoir **enable_object_processing: True** sous **[file_manager]** dans votre fichier **moonraker.conf**.
<br>
Cela permettra à Klipper de traiter les fichiers Gcode entrants pour marquer les objets.
<br>

Cela doit ressebmbler à ceci:
<br>

Moonraker.conf
<br>
```
[file_manager]
enable_object_processing: True
```
<br>

