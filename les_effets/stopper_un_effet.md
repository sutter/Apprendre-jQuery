# Stopper une animation / un effet

Dans cette partie nous verrons la méthode `.stop()` servant à stopper **une animation** ou **un effet**.

## Méthode .stop()

**API :** [http://api.jquery.com/stop/](http://api.jquery.com/stop/)

```js
$(selecteur).stop(stopAll,goToEnd)
```

Cette méthode prend 2 paramètres :

| Paramètre | Description
| -- | -- | -- |
| StopAll | **Optionnelle** : la valeur par défaut est **false**.<br/>Valeur booléenne indiquant **true** ou **false** permettant d'arrêter toutes les animations en file d'attente. |
| goToEnd | **Optionnelle** : la valeur par défaut est **false**.<br/>Valeur booléenne indiquant **true** ou **false** permettant de finir toutes les animations immédiatement. |

### Stop sans paramètre

Prenons l'exemple d'un carré que l'on anime avec la méthode `.animate()` au click sur le bouton *Play*. Si nous cliquons sur le bouton *stop* l'animation en cours se stoppe grâce à la méthode `.stop()` sans paramètres. Au click sur *play* l'animation reprend là ou elle en était.

```js
// Déclaration de l'animation
$('#play').click(function(){
    $('.pod').animate({
        left: '250px',
        width: '+=150px'
    }, 1500)
    .animate({
        opacity: '0.25',
    }, 3000);
});

// Déclaration de la méthode .stop() au click
$('#stop').click(function(){
   $('.pod').stop();
});
```

<p data-height="200" data-theme-id="7816" data-slug-hash="tdECu" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/tdECu/'>.stop()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

Prenons l'exemple d'un carré de l'ont modifie au survol. Dans l'exemple si dessous nous voyons qu'au survol avec de multiples passages sur le carré rose, l'animation continue le nombre de fois survolée, se qui peut être plutôt gênant. Tandis que le carré bleu lui cesse son animation lorsque le survol est terminé.

```js
// Déclaration sans .stop()
$('#a').hover(function(){
    $(this).fadeTo('slow', 0.25);
  },function(){
    $(this).fadeTo('slow', 1);
});

// Déclaration avec .stop()
$('#b').hover(function(){
    $(this).stop().fadeTo('slow', 0.25);
  },function(){
    $(this).stop().fadeTo('slow', 1);
});
```

<p data-height="200" data-theme-id="7816" data-slug-hash="uBGal" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/uBGal/'>.stop() - 2</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

### Stop avec les paramètres 'stopAll' et 'goToEnd'

Reprenons le cas de notre premier exemple. Agrémentons le d'un bouton de stopper les animations en cours et un autre pour les terminer toutes.

```js
// Stopper toutes les animations en cours
$('#stopAll').click(function(){
   $('.pod').stop(true);
});

// Finir toutes les animations en cours
$('#goToEnd').click(function(){
   $('.pod').stop(true, true);
});
```

<p data-height="200" data-theme-id="7816" data-slug-hash="wmuEt" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/wmuEt/'>.stop() - 3</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

<script async src="//codepen.io/assets/embed/ei.js"></script>
