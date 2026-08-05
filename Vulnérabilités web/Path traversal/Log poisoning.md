Le `Log Poisoning`, comme le nom l'indique, est une attaque qui consiste a "empoisonner" les enregistrements(logs), pour permettre a un attaquant d'obtenir un accès sur une machine cible.

Par exemple, un attaquant peut introduire un shell `  <?php system($_GET["cmd"]);?>  `" php simple a l'intérieur d'un fichier du dossier "``  /var/lib/php/sessions/  ``" , ou  encore ``  /var/log/apache2/access.log  `` , ce qui peut être en modifiant la valeur d'un header (`user-agent` par exemple) , ou d'une valeur stockée dans les logs.

Ensuite, il faudrait que l'attaquant requête ces fichiers/dossiers au serveur en exploitant une LFI.


