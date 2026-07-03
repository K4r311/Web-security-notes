La Blind SSRF est une attaque qui consiste a utiliser un serveur intermédiaire pour que celui-ci reçoive les requêtes du serveur front-end.

Par exemple, supposons qu'on a un site web 
  ```
  http://example.com/index.html?url=localhost/
  ``` 
  Ici, on peut déployer un serveur (avec python) qui va recueillir des informations a chaque requête.
  Ensuite, on peut modifier la valeur du paramètre **?url** par l'adresse IP du serveur qu'on possède.
  
