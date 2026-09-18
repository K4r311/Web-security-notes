La faille XSS réfléchi consiste a introduire du javascript dans une valeur entrée par l'utilisateur, qui sera immédiatement **renvoyée au navigateur** dans la prochaine réponse `HTTP`.

Par exemple, imaginons un site web qui possède une zone de recherche, et lorsque l'utilisateur fait la recherche, on a dans la barre d'URL:

`http://example.com/search?=whatever`

Et la valeur du paramètre `search` est refletée a l'écran. Ainsi, on pourrait provoquer une attaque XSS réfléchie en insérant un bout de code dans le contenu de ce paramètre. 

Cela donnerait quelque chose comme:

`http://example.com/search?=<script>/* some malicious code here */</script>`

