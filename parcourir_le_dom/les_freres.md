# Parcourir les frères

Dans cette partie, nous verrons les méthodes `.siblings()`, `.next()`, `.nextAll()`, `.nextUntil()`, `.prev()`, `.prevAll()` et `.prevUntil()`

## Méthode .siblings()

**API :** http://api.jquery.com/siblings/

La méthode `.siblings()` retourne tous les éléments frères de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` aux frères de `class="item"`.

```html
<ul class="list">
    <li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').siblings().addClass('selected');
```

**Résultat**

```html
<ul class="list">
    <li class="selected">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
</ul>
```


## Méthode .next()

**API :** http://api.jquery.com/next/

La méthode `.next()` retourne le frère suivant de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` au frère suivant de `class="item"`.

```html
<ul class="list">
	<li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').next().addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li>…</li>
	<li>…</li>
</ul>
```


## Méthode .nextAll()

**API :** http://api.jquery.com/nextAll/

La méthode `.nextAll()` retourne tous les frères suivants de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` aux frères suivants de `class="item"`.

```html
<ul class="list">
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').nextAll().addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
</ul>
```

## Méthode .nextUntil()

**API :** http://api.jquery.com/nextUntil/

La méthode `.nextUntil()` retourne tous les frères suivants entre les éléments sélectionnés.

L'exemple suivant ajoute `class="selected"` aux frères suivants entre `class="item"` et le `class="other-class"`.

```html
<ul class="list">
    <li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li class="other-class">…</li>
</ul>
```

```js
$('.item').nextUntil('.other-class').addClass('selected');
```

**Résultat**

```html
<ul class="list">
    <li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="other-class">…</li>
</ul>
```

## Méthode .prev()

**API :** http://api.jquery.com/prev/

La méthode `.prev()` retourne le frère prédédent l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` au frère prédédent de `class="item"`.

```html
<ul class="list">
    <li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').prev().addClass('selected');
```

**Résultat**

```html
<ul class="list">
    <li>…</li>
	<li>…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

## Méthode .prevAll()

**API :** http://api.jquery.com/prevAll/

La méthode `.prevAll()` retourne tous les frères prédédents de l'élément sélectionné.

L'exemple suivant ajoute `class="selected"` aux frères prédédents de `class="item"`.

```html
<ul class="list">
	<li>…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').prevAll().addClass('selected');
```

**Résultat**

```html
<ul class="list">
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

## Méthode .prevUntil()

**API :** http://api.jquery.com/prevUntil/

La méthode `.prevUntil()` retourne tous les frères prédédents entre les éléments sélectionnés.

L'exemple suivant ajoute `class="selected"` aux frères prédédents entre `class="item"` et `class="other-class"`.

```html
<ul class="list">
    <li>…</li>
	<li class="other-class">…</li>
	<li>…</li>
	<li>…</li>
	<li class="item">…</li>
	<li>…</li>
	<li>…</li>
</ul>
```

```js
$('.item').prevUntil('.other-class').addClass('selected');
```

**Résultat**

```html
<ul class="list">
    <li>…</li>
    <li class="other-class">…</li>
	<li class="selected">…</li>
	<li class="selected">…</li>
	<li class="item">…</li>
    <li>…</li>
	<li>…</li>
</ul>
```
