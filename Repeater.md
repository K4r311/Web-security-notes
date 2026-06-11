Repeater est une extension de burpsuite, tout comme [[Intruder]]. Repeater permet d'observer les réponses et les requêtes HTTP lancées par le navigateur en temps réel.

Par exemple, après un bruteforce avec intruder pour retrouver les utilisateurs disponibles, on peut faire une requête qui contient un nom d'utilisateur dont on est sur de l'absence sur la platforme cible.

Ainsi, on peut capturer la réponse de la cible suite a cette requête, et faire une recherche négative dans le résultat de Intruder, c'est-a-dire que l'on aura les résultats qui ne conviennent **pas** a notre recherche. Autrement dit, on obtiendrait les utilisateurs qui existent, car ceux qui n'existent pas sont filtrés.

Puisque BurpSuite CE(community edition) ne peut pas faire de recherche négative, on peut sauvegarder la sortie et utiliser grep a la place en faisant:
```bash 
 grep -v "pattern" filename.txt 
```
En effet, 'pattern' désigne l'objet de la recherche négative, et 'filename.txt' est le fichier dans lequel la recherche doit se faire.