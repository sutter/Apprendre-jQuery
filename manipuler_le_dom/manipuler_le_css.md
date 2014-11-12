# Manipuler le CSS

Dans cette partie, nous verrons les méthodes `.addClass()`, `.removeClass()`, `.toogleClass()` et `.css()`.

## Méthode .addClass()

**API :** http://api.jquery.com/addClass/

La méthode `.addClass()` permet d'ajouter une classe sur l'élément selectionné.

L'exemple suivant ajoute la classe `pod` à `class="box"`.

```html
<div class="box">…</div>
```

```js
$('.box').addClass('pod');
```

**Résultat**

```html
<div class="box pod">…</div>
```

Nous pouvons ajouter plusieurs classes en les séparant d'un espace.

```js
$('.box').addClass('pod product');
```

**Résultat**

```html
<div class="box pod product">…</div>
```

Exemple d'ajout de classe au click.

<p data-height="180" data-theme-id="7816" data-slug-hash="qmuCr" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/qmuCr/'>.addClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .removeClass()

**API :** http://api.jquery.com/removeClass/

La méthode `.removeClass()` permet de supprimer une classe sur l'élément selectionné.

L'exemple suivant supprime `class="box pod"`.

```html
<div class="box pod">…</div>
```

```js
$('.box').removeClass();
```

**Résultat**

```html
<div>…</div>
```

Nous pouvons aussi passer le nom d'une classe en paramètres.
Par exemple, ici nous supprimons la classe `.pod` de l'élément `class="box pod"`.

```js
$('.box').removeClass('pod');
```

**Résultat**

```html
<div class="box">…</div>
```

Exemple de supression de class au click.

<p data-height="180" data-theme-id="7816" data-slug-hash="ILbkv" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/ILbkv/'>.removeClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .toggleClass()

**API :** http://api.jquery.com/toggleClass/

La méthode `.toggleClass()` permet d'ajouter une classe sur l'élément selectionné si elle n'est pas présente et inversement.

L'exemple suivant ajoute la classe `.is-active` à `class="btn"` au click, ou la supprime si elle est présente.

```js
$('.btn').click(function(){
    $(this).toggleClass('is-active');
});
```

<p data-height="180" data-theme-id="7816" data-slug-hash="AvzIk" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/AvzIk/'>.toggleClass()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

## Méthode .css()

**API :** http://api.jquery.com/css/

La méthode `.css()` affecte les styles CSS à l'élément sélectionné.

Elle agit aussi comme un *getter* et permet donc d'obtenir la chaîne de caractères de la valeur CSS demandée.

L'exemple suivant ajoute un fond rouge à `class="box"`.

```html
<div class="box">…</div>
```

```js
$('.box').css('background-color','red');
```

**Résultat**

```html
<div class="box" style="background-color: red;">…</div>
```

Nous pouvons bien sûr ajouter plusieurs styles CSS en même temps sous forme d'un objet avec des paramètres.

```js
$('.box').css({
    'background-color': 'red',
    'font-size': '20px',
    'color': 'yellow'
});
```

**Résultat**

```html
<div class="box" style="font-size: 20px; color: yellow; background-color: red;">…</div>
```

### Setter

Comme je l'ai expliqué plus haut, nous pouvons obtenir la valeur d'une propriété CSS comme dans l'exemple ci-dessous.

```html
<div class="box">…</div>
<div class="pod">…</div>
```

```css
.pod { background: red }
```

```js
$('.box').css('background-color', $('.pod').css('background-color') );
```

**Résultat**

```html
<div class="box">…</div>
<div class="pod" style="background-color: red;">…</div>
```

<script async src="//codepen.io/assets/embed/ei.js"></script>


