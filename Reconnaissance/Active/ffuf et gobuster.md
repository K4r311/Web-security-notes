ffuf et gobusters sont des outils utilisés en reconnaissance active, principalement pour fuzzer les sous domaines et dossiers sur une application web.
Pour trouver les répertoires/dossiers , utiliser la commande:
```bash
ffuf -c -w /usr/share/wordlists/dirb/common.txt -u 'http://target_ip/FUZZ'
```
Pour trouver les sous domaines, gobuster est préféré. Ainsi, la commande est:
```bash
gobuster dns --domain example.com -w wordlist.txt
```

Après cela, on peut utiliser [[Intruder]] ou [[hydra]] pour le bruteforce de login si il y en a un.


