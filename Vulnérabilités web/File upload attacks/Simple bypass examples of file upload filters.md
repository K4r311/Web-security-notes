Les vulnérabilités liées a l'upload de fichier sont des failles qui ont lieu lorsque le serveur accepte qu'un fichier sensible soit téléversé.

Ces vulnérabilités ne sont pas critiques juste parce qu'un fichier restreint peut être ajouté en esquivant les filtres, mais le **risque** est dans la manière dont **ces fichiers sont interprètés par le serveur.** 

---
<u>Les filtres commun sont et leur bypass sont:</u>

-`Content-Type` header côté client : Valeur modifiable en utilisant un proxy ([[ZAP]] , BurpSuite, Caido par exemple)

-Vérification de l'extension: peut être changée très facilement, On peut renommer`shell.php` en `shell.php.png` , en considérant que `.png` est l'extension acceptée.

-Vérification des "Magic-Bytes": Peuvent être modifiés en utilisant des outils comme `hexeditor`.

-Les bypass comme ".PnG" au lieu de ".png"(on joue avec les caractères).
