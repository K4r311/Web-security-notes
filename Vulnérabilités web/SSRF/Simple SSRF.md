La faille SSRF(Server Side request forgery) est une vulnérabilité web. Elle permet a un attaquant de modifier les requêtes HTTP pour que le serveur envoie des requêtes au backend ou a un autre serveur pour ensuite sortir des informations sensibles.

Par exemple, supposons que nous avons un serveur qui vérifie une valeur avant de l'envoyer. Le paramètre utilisé peut être:
```
Value=http://stock.vulnerable.com:8080/product/stock/check%3FproductId%3D6%26storeId%3D1
```
L'attaquant peut modifier la valeur de "`Value`"par  http:/localhost/admin ou autre page sensible, ce qui lui accorde des permissions élevées.

[[SSRF on a back-end system]]
