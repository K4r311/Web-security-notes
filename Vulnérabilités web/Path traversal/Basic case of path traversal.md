Le "Path traversal"(ou parcours de répertoires) est une vulnérabilité web qui permet a un utilisateur de manipuler et/ou de lire des fichiers directement sur le serveur.

Par exemple, supposons qu'une page web est telle que: ```http://vulnerable-site.com/files?filename=image.png``` . Ici, un attaquant peut modifier '```image.png```' et mettre ```../../../etc/passwd/``` pour lire les mots de passe du système.

Note: Le nombre que fois où il faut reculer avec ../ dépend de la position de l'utilisateur lorsqu'il lit ``image.png`` dans notre cas.
