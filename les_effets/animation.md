# Animation

Dans cette partie nous verrons la méthode `.animate()`, qui sert à céer des animation personnalisées.

## Méthode .animate()

**API** : [http://api.jquery.com/animate/](http://api.jquery.com/animate/)

```js
$(selecteur).animate({paramètres},vitesse,callback);
```

Par exemple déplaçons un élément **class="pod"** de 250px ver la droite.

```js
$('#play').click(function(){
    $('.pod').animate({left: '250px'}, 500);
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="uidws" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/uidws/'>.slideToggle()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>


Les animations peuvent aussi être plus complexes.<br/>
Comme dans l'exemple ci-dessus, nous déplaçons **class="pod"** vers la droite et nous agrandissons sa largeur de 150px en même temps.

```js
$('#play').click(function(){
    $('.pod').animate({
        left: '250px',
        width: '+=150px'
    }, 500);
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="feBrl" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/feBrl/'>.animate() - 2</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

Nous pouvons aussi rajouter un callback.

```js
$('#play').click(function(){
    $('.pod').animate({
        left: '250px',
        width: '+=150px'
    }, 500, function(){
		alert("L'animation est terminée");
	});
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="oxvek" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/oxvek/'>.animate() - 3</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Chaîner deux animations

Nous avons la possibilité avec la méthode `.animate()` de chaîner les animations, c'est-à-dire de lancer une animation, puis une autre.

Continuons de complexifier l'exemple du dessus.
À la fin de l'animation **class="pod"** prends une opacité de 25%.

```js
$('#play').click(function(){
    $('.pod').animate({
        left: '250px',
        width: '+=150px'
    }, 500)
    .animate({
        opacity: '0.25'
    }, 1000);
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="BGxpf" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/BGxpf/'>.animate() - 4</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

Nous pouvons aussi lancer les deux animations en même temps en fixant le paramètre `queue`à `false`. Cela aura pour effet de ne plus mettre l'animation ciblée à la queue.

```js
$('#play').click(function(){
    $('.pod').animate({
        left: '250px',
        width: '+=150px'
    }, 500)
    .animate({
        opacity: '0.25',
    }, {
		'queue': false,
		'duration': 1000
	};
});
```
<p data-height="200" data-theme-id="7816" data-slug-hash="mcuqi" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/mcuqi/'>.animate() - 5</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>
