# Les fondus

Dans cette partie nous verrons les méthodes `.fadeIn()`, `.fadeOut()`, .fadeToggle()` et `.fadeTo()`. Elles servent à faire apparaître ou disparaître des éléments avec une animation de fondu.

## Méthode .fadeIn()

**API** : [http://api.jquery.com/fadeIn/](http://api.jquery.com/fadeIn/)

La méthode `.fadeIn()` permet faire apparaître les éléments avec une animation de fondu.

```js
$(selecteur).fadeIn(vitesse,callback);
```

Exemple :

```js
$('#fadeIn').click(function(){
    $('#a').fadeIn();
    $('#b').fadeIn(1000);
    $('#c').fadeIn('slow');
    $('#d').fadeIn('slow', function(){
        console.log('Élément #d est apparu);
    });
});
```
<p data-height="180" data-theme-id="7816" data-slug-hash="KLxjB" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/KLxjB/'>.fadeIn()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .fadeOut()

**API** : [http://api.jquery.com/fadeOut/](http://api.jquery.com/fadeOut/)

La méthode `.fadeOut()` permet faire disparaître les éléments avec une animation de fondu.

```js
$(selecteur).fadeOut(vitesse,callback);
```

Exemple :

```js
$('#fadeOut').click(function(){
    $('#a').fadeOut();
    $('#b').fadeOut(1000);
    $('#c').fadeOut('slow');
    $('#d').fadeOut('slow', function(){
        console.log('Élément #d à disparu);
    });
});
```
<p data-height="180" data-theme-id="7816" data-slug-hash="yaric" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/yaric/'>.fadeOut()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .fadeToggle()

**API** : [http://api.jquery.com/fadeToggle/](http://api.jquery.com/fadeToggle/)

La méthode `.fadeToggle()` permet faire apparaître / disparaître les éléments avec une animation de fondu.

```js
$(selecteur).fadeToggle(vitesse,callback);
```

Exemple :

```js
$('#fadeToggle').click(function(){
    $('#a').fadeToggle();
    $('#b').fadeToggle(1000);
    $('#c').fadeToggle('slow');
    $('#d').fadeToggle('slow', function(){
        console.log('Élément #d est apparu / à disparu');
    });
});
```
<p data-height="180" data-theme-id="7816" data-slug-hash="ckEap" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/ckEap/'>.fadeToggle</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

## Méthode .fadeTo()

**API** : [http://api.jquery.com/fadeTo/](http://api.jquery.com/fadeTo/)

La méthode `.fadeTo()` permet modifier l'opacité d'un élément avec un effet de transition.

```js
$(selecteur).fadeTo(vitesse,callback);
```

Exemple :

```js
$('#fadeTo').click(function(){
    $('#b').fadeTo(1000, 0.25);
    $('#c').fadeTo('slow', 0.25);
    $('#d').fadeTo('slow', 0.25, function(){
        console.log('Élément #d à une opacité de 25%);
    });
});
```

<script async src="//codepen.io/assets/embed/ei.js"></script>
