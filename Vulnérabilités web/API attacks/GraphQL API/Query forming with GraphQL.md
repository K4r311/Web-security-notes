Les API graphQL reçoivent des requêtes dont la structure diffère de celles des API REST. Elles ressembles généralement à:
```graphQL
query GetUser($userId: ID!) { 
user(id: $userId) { 
id 
name 
email 
} 
}
```
Aussi, peut-on changer la valeur des paramètres pour un résultat plus préférable.
