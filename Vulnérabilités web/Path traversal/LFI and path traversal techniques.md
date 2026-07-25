Sur certaines applications web, le path traversal est possible, mais l'application bloque les commandes de changement de répertoire lorsqu'elles sont brutes. On peut donc faire un "URL encode" sur le payload.
Il est préféré d'encoder deux fois.

Il est également possible d'utliser un null-byte pour modifier l'extension du fichier. Par exemple, ``filename=../../../etc/passwd%00.png``  

On peut aussi utiliser "`....//`" a la place de "`../`" , dans le cas où l'application enlève juste ../ du chemin, puisque ça pourrait laisser le "`../`", même après le filtre.

