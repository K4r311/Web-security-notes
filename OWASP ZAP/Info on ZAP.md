
OWASP zap(Zed Attack Proxy) est une alternative a BurpSuite.(donc il fait ce que [[Intruder]] et [[Repeater]] font), cet outil:
-Permet également le crawling sur les applications web.
-Détecte les vulnérabilités après le crawling

Pour configurer le proxy dans zap(**HTTP**), il faut:
**1ere OPTION:**
-Ouvrir ZAP
-Aller dans l'onglet "Tools" puis "Options"
-Aller dans 'Local proxies' puis définir l'addresse du proxy et le port sur lequel il tourne
-Aller dans 'Server certificate' pour obtenir un certificat, puis le sauvegarder dans un endroit sur.
-utiliser le certificat dans les paramètres réseau de firefox

**2e OPTION:**
-Installer Foxyproxy
-Aller dans l'onglet "options" ou  autre similaire selon la version. Ceci va ouvrir un dashboard pour gérer foxyproxy
-Accéder a l'onglet "proxies"
-Configurer un proxy avec un port, adresse IP (localhost), et un nom.


Important: Le certificat peut se montrer nécessaire lorsqu'on travaille avec https.
