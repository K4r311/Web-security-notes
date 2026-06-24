XSS(Cross-Site scripting) est une vulnérabilité côté client. Elle consiste a injecter du code, généralement du JavaScript dans une application web. Ce code peut être utilisé pour voler des identifiants(mots de passe, cookies)pour ensuite procéder a un [[Bruteforce de cookies]], ou donner un accès non attendu a un attaquant.

En pratique, les vulnérabilités XSS peuvent être exploitées sur les applications web où l'utilisateur a la possibilité d'upload du texte. Cela peut être un commentaire laissé sur un réseau social, post, ou n'importe quelle information accessible par la victime.

Pour y remédier, on peut donc forcer le navigateur a transformer le code html en texte avant de l'exécuter.
