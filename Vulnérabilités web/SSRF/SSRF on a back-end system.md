La faille SSRF peut aussi être utilisée sur toute une infrastructure backend. Lorsque le serveur front-end reçoît la demande de l'utilisateur, il envoie une autre requête au back-end en fonction de ce que l'utilisateur veut.

Pour cela, l'attaquant peut scanner le subnet, trouver des machines actives, et utiliser le paramètre ou le header responsable de la SSRF pour accéder aux serveurs, et y envoyer des requêtes.

Par exemple, un attaquand peut accéder a un endpoint ``` http://192.168.0.230:80/admin``` en utilisant la SSRF.