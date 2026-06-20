Certaines applications web refusent qu'une même addresse IP envoie plusieurs tentatives de connection consécutives échouées.

Mais ceci peut être contourné en modifiant notre addresse IP dans les headers HTTP. Les headers responsables de l'addresse IP sont généralement ceux comme ```X-Forwarded-For``` . 

Nous pouvons donc générer une liste d'addresses IP et modifier la valeur a chaque tentative, ce qui fera croire au serveur que la requête vient de quelqu'un d'autre.
