Les injections SQL booléennes se basent sur deux états (true/false) pour fonctionner. Au cours d'une injection SQL booléenne, on observe si la page cible ou le code source a subi une modification. En fonction de cette différence, on peut deviner si notre requête a un résultat positif ou non:
```SQL
target' UNION SELECT 1,2,3 where database() like 's%';--
```
le payload demande au serveur de renvoyer les bases de données ou le nom commence par 's'. On observe la réponse(true/false) et on va par tatonnement, en essayant de deviner le nom de la table.

Après avoir trouvé le nom d'une base de données, il faut répéter le meme processus avec les tables, colonnes, et enfin extraire un nom d'utilisateur, mot de passe.

Ce type d'attaque est similaire aux [[union-based SQLi]] au moment d'énumérer la base de données.

