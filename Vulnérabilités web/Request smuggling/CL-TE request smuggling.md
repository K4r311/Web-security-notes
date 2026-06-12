Le request smuggling de type CL(content length)-TE(transfer encoding ) fait penser au serveur front-end qu'une seule requête est envoyée, et ce serveur se concentre sur le header **content length**. Ensuite, celui du backend prendra le header **transfer encoding**. Si une deuxième requête malveillante est cachée, elle peut être excutée:
```http
POST / HTTP/1.1
Host: httprequestsmuggling.thm
Content-Type: application/x-www-form-urlencoded
Content-Length: 160
Transfer-Encoding: chunked

0

POST /contact.php HTTP/1.1
Host: httprequestsmuggling.thm
Content-Type: application/x-www-form-urlencoded
Content-Length: 500

username=test&query=§
```
Un exemple est ci-dessus. En effet, ici, le serveur front-end voit la valeur du header 'content-length' et le laisse passer car la valeur est bonne. Le backend traite le header "transfer-encoding" de la première requête et considère qu'elle s'arrête au 0.
 Cependant, il exécute par la suite la requête "POST /contact.php HTTP/1.1" car il considère que c'est une nouvelle requête. Mais celle-ci n'est pas filtrée par le serveur du frontend. On peut dire qu'on a bypass le serveur frontend.
 
