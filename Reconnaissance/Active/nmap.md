Nmap(network mapper) est un outil en ligne de commande qui permet de trouver les ports ouverts sur une machine, détecter les services, leurs versions qui tournent, et permet même de 'mapper' un sous réseau.
```bash 
nmap -A -p- -T4 'target_ip'
```
Après le scan, il se pourrait que http soit disponible, et c'est ici qu'interviennent [[ffuf et gobuster]]. 