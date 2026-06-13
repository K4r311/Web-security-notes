Ces  injections SQL utilisent le temps comme repère, tel leur nom indique. Les time-based SQLi utilisent la méthode SLEEP() de SQL pour avoir un écart entre les résultats positifs et ceux négatifs.
Par exemple, on se débrouille pour que la requête du backend soit:
```SQL
select * from 'target_table' where domain='target_user' UNION SELECT SLEEP(5),2;--' LIMIT 1
```
Ici, la méthode est similaire a celle des injections booléennes, mais la particularité est la fonction SLEEP(). On reprend donc la procédure pour obtenir les tables, les colonnes, et enfin leur contenu.

Aussi, des Outils tels que SQLmap facilitent ce type d'injection.
