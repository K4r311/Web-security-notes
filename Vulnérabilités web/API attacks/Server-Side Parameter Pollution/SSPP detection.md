La SSPP (Server-Side Parameter Pollution) est une vulnérabilité qui permet de redéfinir la valeur d'un ou plusieurs paramètres au niveau d'un endpoint API.

Par exemple, considérons une requête telle que:
```
GET /api/users?name=target
```

---------------------
Pour tester si une SSPP est disponible, on peut utiliser le caractère `#` pour "couper" la requête(le caractère # a été encodé en URL):
```
GET /api/users?name=target%23test
```
Si l'application prend "target" uniquement comme nom, une SSPP est probablement possible.

---
On peut également tenter une attaque similaire avec le caractère `&`, mais seulement si un paramètre a tester a pu être identifié.

**Note**: Faire attention aux fichiers JavaScript qui peuvent être identifiés sur le site web.
