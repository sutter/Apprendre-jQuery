# Manipuler le CSS

Dans cette partie, nous verrons les méthodes `.addClass()`, `.removeClass()`, `.toogleClass()` et `.css()`.

## Méthode .addClass()

**API :** http://api.jquery.com/addClass/

La méthode `.addClass()` permet d'ajouter une classe sur l'élément selectionné.

L'exemple suivant ajoute la classe `pod` à `class="box"`.

```js
$('.box').addClass('pod');
```

Nous pouvons ajouter plusieurs classes en les séparant d'un espace.

```js
$('.box').addClass('pod product');
```
Exemple d'ajout de classe au click.

<p data-height="180" data-theme-id="7816" data-slug-hash="qmuCr" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/qmuCr/'>.addClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .removeClass()

**API :** http://api.jquery.com/removeClass/

La méthode `.removeClass()` permet de supprimer une classe sur l'élément selectionné.

L'exemple suivant supprime `class="box"`.

```js
$('.box').removeClass();
```

Nous pouvons aussi passer le nom d'une classe en paramètre.
Par exemple ici nous supprimons la classe `.product` de l'élément `class="box"`.

```js
$('.box').removeClass('product');
```

Exemple de supression de class au click.

<p data-height="180" data-theme-id="7816" data-slug-hash="ILbkv" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/ILbkv/'>.removeClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .toggleClass()

**API :** http://api.jquery.com/toggleClass/

La méthode `.toggleClass()` permet d'ajouter une classe sur l'élément selectionné si elle n'est pas présente et inversement.

L'exemple suivant ajoute la classe `.is-active` à `class="btn"` au click, ou la supprime si elle est présente.

```js
$('#a').click(function(){
    $('#b').toggleClass('bg-success');
});
```

<p data-height="180" data-theme-id="7816" data-slug-hash="AvzIk" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/AvzIk/'>.toggleClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .css()

**API :** http://api.jquery.com/css/

La méthode `.css()` affecte les style CSS à l'élément selectionné.
Elle agit aussi comme un *getter*, et permet donc d'obtenir la chaîne de caractère de la valeur CSS demandée.

L'exemple suivant ajout un fond rouge à `class="box"`.

```js
$('.box').css('background-color','red');
```

Nous pouvons bien sûr ajouté plusieurs style CSS en même temps, sous forme de tableau.
```js
$('.box').css({
    'background-color': 'red',
    'font-size': '20px',
    'color': 'yellow'
});
```

Comme je l'ai expliquer plus haut, nous pouvons obtenir la valeur d'une propriété CSS comme dans l'exemple ci-dessous.

```js
$('.box').css('background-color', $('.pod').css('background-color') );
```
<script async src="//codepen.io/assets/embed/ei.js"></script>


