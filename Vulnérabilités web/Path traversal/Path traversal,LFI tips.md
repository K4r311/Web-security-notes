-L'URL encoding (double si possible)
-L'utilisation des "`....//` " a la place des "`../`"
-Rester sous le dossier attendu par l'app web au lieu de changer tout le chemin. 
-Utiliser les wrappers php, par exemple: 
```
php://filter/read=convert.base64-encode/resource=sensitive_file
```
pour encoder le fichier en base 64, afin d'éviter qu'il soit exécuté par l'application web.
