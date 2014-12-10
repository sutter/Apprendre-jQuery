# Plier / Déplier

Dans cette partie, nous verrons les méthodes `.slideDown()`, `.slideUp()` et `.slideToggle()`. Elles permettent de plier et déplier des éléments avec une animation de fondu.

## Méthode .slideDown()

**API** : [http://api.jquery.com/slideDown/](http://api.jquery.com/slideDown/)

La méthode `.slideDown()` permet de déplier un élément avec une transition.

```js
$(selecteur).slideDown(vitesse,callback);
```

**Exemple :**

```js
$('#slideDown').click(function(){
    $('#a').slideDown();
    $('#b').slideDown(1000);
    $('#c').slideDown('slow');
    $('#d').slideDown('slow', function(){
        console.log('Élément #d est déplié');
    });
});
```

**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="jCkdJ" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/jCkdJ/'>.slideDown()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .slideUp()

**API** : [http://api.jquery.com/slideUp/](http://api.jquery.com/slideUp/)

La méthode `.slideUp()` permet de replier un élément avec une transition.

```js
$(selecteur).slideUp(vitesse,callback);
```

**Exemple :**

```js
$('#slideUp').click(function(){
    $('#a').slideUp();
    $('#b').slideUp(1000);
    $('#c').slideUp('slow');
    $('#d').slideUp('slow', function(){
        console.log('Élément #d est plié');
    });
});
```
**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="yBCDA" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/yBCDA/'>SlideUp</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>


## Méthode .slideToggle()

**API** : [http://api.jquery.com/slideToggle/](http://api.jquery.com/slideToggle/)

La méthode `.slideToggle()` permet de plier / déplier un élément avec une transition.

```js
$(selecteur).slideToggle(vitesse,callback);
```

**Exemple :**

```js
$('#slideToggle').click(function(){
    $('#a').slideToggle();
    $('#b').slideToggle(1000);
    $('#c').slideToggle('slow');
    $('#d').slideToggle('slow', function(){
        console.log('Élément #d est plié / déplié');
    });
});
```

**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="pCDuH" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/pCDuH/'>.slideToggle()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

<script async src="//codepen.io/assets/embed/ei.js"></script>
