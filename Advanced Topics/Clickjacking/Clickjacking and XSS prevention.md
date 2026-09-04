Pour contrer les failles de clickjacking, il faut:
- Utiliser les `X-frame-options`, car ce header permet d'accepter l'utilisation des iframes ou non.
- Utiliser les headers `Content-Security-Policy`: leur rôle est de définir quelle ressource le navigateur est censé considérer en chargeant la page. Ce header peut aussi être combiné aux directives `frame-ancestors` , assez similaires aux X-frame-options.
