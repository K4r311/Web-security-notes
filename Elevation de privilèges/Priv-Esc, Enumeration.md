# Operating System Enumeration


<u>Commandes</u>:
Pour trouver le  **nom de l'hôte**,**le système d'exploitation** et la **version du kernel,** lancer la commande:
```
uname -a 
```
Pour trouver les processus qui sont actifs sur la machine, lancer:
```
ps [OPTIONS]
```
Options:
 Les processus de tous les utilisateurs: `a`
Utilisateurs responsables du processus: `u`
Processus non-liés au terminal:`x`
output en arborescence:`f`
output en format "job":`j`

<u>Fichiers et dossiers</u>:
`/etc/issue`: version et OS de la machine
`/etc/crontab` : cron jobs sur la machine

`/var/spool/cron/` : dossier contenant les fichiers spécifiques aux cron-jobs des utilisateurs
`/etc/cron.d/` : utilisé par l'OS pour réguler les cron jobs.

# User Enumeration
<u>Commandes</u>: 
Pour avoir des infos sur un utilisateur et son groupe:
```
id [username]
```
la commande `id` seule permet d'avoir des infos sur l'utilisateur actuel.

Pour trouver les variables d'environnement: 
``` 
env 
```
Pour trouver les commandes qui peuvent être lancées en tant que sudo:
```
sudo -l
```
Pour trouver l'historique des commandes:
``` 
history
```
<u>Fichiers</u>:
/etc/passwd : Contient une liste des utilisateurs présents sur la machine

# Network Enumeration
`netstat` permet d'avoir des informations sur les ports, l'interface réseau de la machine. Lancer `netstat -h` pour plus d'informations.
