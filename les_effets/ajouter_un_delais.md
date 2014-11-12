# Ajouter un délais

Dans cette partie, nous verrons la méthode `.delay()` servant à ajouter un délais avant l'exécution d'un effet.

## Méthode .delay()

**API :** http://api.jquery.com/delay/

```js
$(selecteur).delay(Durée)
```

Prenons le cas de deux éléments **#a** et **#b**, qui reçoivent successivement une méthode `.slideUp()`puis `.slideDown()`. Nous ajoutons à l'élément **#b** une méthode `.delay(1000)` entre les deux méthodes de *slide*. Nous pouvons nous rendre compte qu'au clic sur le bouton, les effets de **#a** sont successifs, tandis que pour **#b** il y a une temporisation de 1s entre les deux.

```js
$('#play').click(function(){

    // Pas de .delay()
    $('#a').slideUp().slideDown();

    // Avec .delay()
    $('#b').slideUp().delay(1000).slideDown();

});
````

<p data-height="266" data-theme-id="7816" data-slug-hash="aFthI" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/aFthI/'>.delay</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

Pour information la méthode `.delay()` ne s'applique qu'aux effets. Pour temporiser d'autres méthodes, il convient d'employer la fonction JavaScript [setTimeout](https://developer.mozilla.org/fr/docs/DOM/window.setTimeout).
