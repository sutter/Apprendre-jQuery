# Les filtres

Dans cette partie, nous verrons les méthodes `.first()`, `.last()`, `.eq()`, `.filter()` et  `.not()`.

## Méthode .first()

**API :** http://api.jquery.com/first/

La méthode `.first()` retourne le premier élément de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` au premier élément de `class="item"`.

```js
$('.item').first().addClass('selected');
```

**Résultat**

```html
<ul class="list">
    <li class="item selected">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
</ul>
```

## Méthode .last()

**API :** http://api.jquery.com/last/

La méthode `.last()` retourne le dernier élément de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` au dernier élément de `class="item"`.

```js
$('.item').last().addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item selected">…</li>
</ul>
```

## Méthode .eq()

**API :** http://api.jquery.com/eq/

La méthode `.eq()` retourne un élément avec un numéro d'index spécifique.
Les numéros d'index commencent à 0, de sorte que le premier élément aura le numéro d'index 0 et non 1.

L'exemple suivant ajoute `class="selected"` au 2ème élément de `class="item"`.

```js
$('.item').eq(1).addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li class="item">…</li>
	<li class="item selected">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
</ul>
```

## Méthode .filter()

**API :** http://api.jquery.com/filter/

La méthode `.filter()` permet de spécifier un critère. Les éléments qui ne correspondent pas aux critères sont retirés de la sélection, et ceux qui correspondent seront retournés.

L'exemple suivant ajoute `class="selected"` aux éléments `class="item"` ayant une autre `class="other-class"`.

```js
$('.item').filter('.other-class').addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="item other-class selected">…</li>
	<li class="item">…</li>
	<li class="item other-class selected">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
</ul>
```

## Méthode .not()

**API :** http://api.jquery.com/not/

La méthode `.not()` retourne tous les éléments qui ne correspondent pas aux critères.
C'est le contraire de la méthode `.filter()`

L'exemple suivant ajoute `class="selected"` qui ne sont pas `li` ayant aucune classe.

```js
$('li').not('.item').addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
</ul>
```
