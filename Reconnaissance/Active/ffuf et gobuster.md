ffuf et gobusters sont des outils utilisés en reconnaissance active, principalement pour fuzzer les sous domaines et dossiers sur une application web.
Pour trouver les répertoires/dossiers , utiliser la commande:
```bash
ffuf -c -w /usr/share/wordlists/dirb/common.txt -u 'http://target_ip/FUZZ'
```
Pour trouver les sous domaines, gobuster est préféré. Ainsi, la commande est:
```bash
gobuster dns --domain example.com -w wordlist.txt
```
Pour trouver les vhosts, on peut:
```
ffuf -u http://TARGET-IP/ -H "Host: FUZZ.example.com" -w /path/to/wordlist.txt
```

Note: pour filtrer les résultats, utiliser les flags:

`-fs` pour filtrer en fonction de la taille, 
`-fc` pour filtrer en fonction du "status code"

