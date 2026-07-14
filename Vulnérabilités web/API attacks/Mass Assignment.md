Les vulnérabilités "Mass Assignment" sont des bugs où le serveur back-end suit aveuglément la requête de l'utilisateur a travers l'API

Par exemple, Imaginons une API sur un formulaire de LogIn. Lorsque l'utilisateur s'authentifie, la requête de l'API contient du JSON tel que:
```
{
"username": "NormalUser" 
"password": "letmein"
"IsAdmin": False
}
```

Si  `"IsAdmin":False` est changé en `"IsAdmin":True` , l'utilisateur `NormalUser` peut se retrouver avec des permissions élevées si le backend accepte tout ce que l'API envoie.

----------------
Dans d'autres cas, les paramètres JSON utilisés niveau de l'API n'apparaissent pas tous au niveau de la requête `POST`,`PUT`,`PATCH` qui est envoyée. 

Une requête `GET` doit être envoyée au niveau de l'endpoint pour exposer les autres paramètres.