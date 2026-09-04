Le `Frame busting` est une technique de prévention contre le clickjacking. 

Cette technique consiste à ajouter un code Javascript a une page web, pour que celle-ci soit la "`top level window`"(fenètre principale), même lorsqu'elle est importée avec les `iframes` .
Le script utilisé était:
```javascript
if (window.top !== window.self) {
    window.top.location = window.self.location;
}
```

---

Les restrictions de ce script peuvent être facilement contournées en utilisant le paramètre `sandbox` des balises `<iframes>` :

`sandbox="allow-forms"`: permet de remplir des formulaires dans la sandbox.
