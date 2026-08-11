Git dumper est un outil qui permet de récupérer le dossier .git d'un serveur, afin de lire le contenu de ce dossier.

Pour dumper un dossier `.git` , on peut lancer la commande:
```bash
git-dumper https://<TARGET_WEBSITE>/.git/ ./<YOUR NEW DIRECTORY NAME>
```

Pour retracer l'historique des commits:
```bash
git log --online --all
```
