Les injections SQL booléennes se basent sur deux états (true/false) pour fonctionner. Au cours d'une injection SQL booléenne, on observe si la page cible a subi une modification. En fonction de cette différence, on peut deviner si notre requête a un résultat positif ou non:
```SQL
select * from users where username = 'target' UNION SELECT 1;--`
```
Notons qu'il faut remplacer 'target' par la valeur de l'utilisateur ciblé, au niveau du champ du nom de l'utilisateur. Il faut également augmenter au fur et a mesure la valeur de l'index ( les chiffres après UNION).
Ce type d'attaque fait recours aux [[union-based SQLi]] au moment d'énumérer la base de données.
