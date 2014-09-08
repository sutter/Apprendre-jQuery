# Notions indispensables

## Les fonctions de rappel

Les fonctions de rappel ou **callback** sont des fonctions qui s'exécutent lorsque l'autre fonction se termine.

Prenons l'exemple ci-dessous, au clic sur un bouton nous faisons disparaître un texte, puis nous affichons un texte dans une boite d'alerte.

```js
$('button').click(function(){
    $('.bg-muted').hide('slow',function(){
      alert('Le paragraphe est maintenant caché');
    });
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="JFxlm" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/JFxlm/'>JFxlm</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

## Chainage de méthodes


Il est possible d'appliquer plusieurs méthodes les unes à la suite des autres.

Plutôt que d'écrire les instructions comme ceci :

```js
$('.box').addClass('is-collapsed');
$('.box').slideUp();
```

Optimisez votre code comme cela :

```js
$('.box').addClass('is-collapsed').slideUp();
```

Vous pouvez même faire des choses plus complexes.<br/>
Par exemple, ajouter une classe `.active` sur un élément au clic, puis faire une recherche dans ce *pattern* pour rechercher un élément qui a la classe `.inner` pour lui supprimer sa classe.

```js
$('.btn').click(function(){
    $(this).addClass('active').find('.inner').removeClass();
    return false;
});
```

<p data-height="200" data-theme-id="7816" data-slug-hash="mjqnx" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/mjqnx/'>mjqnx</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>
