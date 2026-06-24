Une IDOR (Insecure Direct Object Reference) est une vulnérabilité web qui permet a un utilisateur d'avoir accès a des objets auquels il ne doit pas avoir accès,en modifiant la requête HTTP que son appareil envoie. Autrement dit, il amène la base de données a envoyer des objets qui devraient normalement être bloqués d'accès par l'attaquant.

Elle être possible lorsque l'application web ne vérifie pas les permissions des utilisateurs avant d'envoyer des réponses. Cette vulnérabilité est souvent sur les pages web du genre: "http://example.com/users/1", ou la modification du 1 en 2 donne accès a un autre profil.

Aussi, cette vulnérabilité ne concerne pas que les comptes utilisateurs, mais autre donnée confidentielle qui peut etre accédée en modifiant la requête.
