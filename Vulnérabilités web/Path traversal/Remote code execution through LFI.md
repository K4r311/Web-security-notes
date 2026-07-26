Pour obtenir une RCE en exploitant une faille LFI, on peut suivre ces étapes:

1- Tout d'abord, exploiter le paramètre vulnérable pour lire les fichiers de configuration. SI c'est du `PHP` , il est conseillé d'encoder le contenu du fichier(par exemple en `base64`) afin d'éviter qu'il ne s'exécute.

2- Lire le fichier de configuration. et être attentif aux options/methodes qu'il utilise, surtout pour du php.

3- Pour la LFI, utiliser les wrappers php comme `filter://`,`data://` ,`expect://`, etc.

4- Utiliser un shell basique en php (`<?phpsystem($_GET["cmd"]);?>`), et encoder en base64, pour que le payload puisse atteindre le serveur sans modification par http.

5- Ajouter le paramètre "cmd"(comme l'indique la commande ci-dessus)