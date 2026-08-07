La fonction d'upload de fichiers peut aussi être utilisé pour réécrire un fichier de configuration. 
En effet, si l'application web est mal protégée, un attaquant peut écraser le contenu d'un fichier système(`.htacess`)  par exemple, afin de permettre au serveur d'exécuter une catégorie donnée de fichiers malveillants, en ajoutant
```
 AddType application/x-httpd-php .php
```
Pour permettre l'exécution de fichiers `.php`
