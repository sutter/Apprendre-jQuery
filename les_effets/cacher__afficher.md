# Cacher / Afficher

Dans cette partie, nous verrons les méthodes `.hide()`, `.show()` et `.toggle()`.

Elles permettenet de faire apparaître ou disparaître des éléments avec une animation.

Ces méthodes peuvent prendre comme paramètres :
1. une vitesse
2. un callback


## Méthode .hide()

**API** : [http://api.jquery.com/hide/](http://api.jquery.com/hide/)

La méthode `.hide()` permet de cacher les éléments.

```js
$(selecteur).hide(vitesse,callback);
```

**Exemple :**

```js
$('#hide').click(function(){
    $('#a').hide();
    $('#b').hide(1000);
    $('#c').hide('slow');
    $('#d').hide('slow', function(){
        console.log('Élément #d est caché');
    });
});
```

**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="mehai" data-default-tab="result" class='codepen'>8ee the Pen <a href='http://codepen.io/sutterlity/pen/mehai/'>mehai</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .show()

**API** : [http://api.jquery.com/show/](http://api.jquery.com/show/)

La méthode `.show()` permet d'afficher les éléments.

```js
$(selecteur).show(vitesse,callback);
```

**Exemple :**

```js
$('#show').click(function(){
    $('#a').show();
    $('#b').show(1000);
    $('#c').show('slow');
    $('#d').show('slow', function(){
        console.log('Élément #d est affiché');
    });
});
```

**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="rfkcI" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/rfkcI/'>rfkcI</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .toggle()

**API** : [http://api.jquery.com/toggle/](http://api.jquery.com/toggle/)

La méthode `.toggle()` permet de cacher / afficher les éléments.

```js
$(selecteur).toggle(vitesse,callback);
```


**Exemple :**

```js
$('#toggle').click(function(){
    $('#a').toggle();
    $('#b').toggle(1000);
    $('#c').toggle('slow');
    $('#d').toggle('slow', function(){
        console.log('Élément #d est caché/affiché');
    });
});
```

**Un autre exemple :**

<p data-height="180" data-theme-id="7816" data-slug-hash="ycxAC" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/ycxAC/'>.toggle</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

<script async src="//codepen.io/assets/embed/ei.js"></script>
