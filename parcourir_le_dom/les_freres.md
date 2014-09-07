# Parcourir les frères

Dans cette partie, nous verrons les méthodes `.siblings()`, `.next()`, `.nextAll()`, `.nextUntil()`, `.prev()`, `.prevAll()` et `.prevUntil()`

## Méthode .siblings()

**API :** http://api.jquery.com/siblings/

La méthode `.siblings()` retourne tous les éléments frères de l'élément sélectionné.

L'exemple suivant ajoute `class="pod"` aux frères de `class="item"`.

```js
$('.item').siblings().addClass('pod');
```

## Méthode .next()

**API :** http://api.jquery.com/next/

La méthode `.next()` retourne le frère suivant de l'élément sélectionné.

L'exemple suivant ajoute `class="pod"` au frère suivant de `class="item"`.

```js
$('.item').next().addClass('pod');
```

## Méthode .nextAll()

**API :** http://api.jquery.com/nextAll/

La méthode `.nextAll()` retourne tous les frères suivants de l'élément sélectionné.

L'exemple suivant ajoute `class="pod"` aux frères suivants de `class="item"`.

```js
$('.item').nextAll().addClass('pod');
```

## Méthode .nextUntil()

**API :** http://api.jquery.com/nextUntil/

La méthode `.nextUntil()` retourne tous les frères suivants entre les éléments sélectionnés.

L'exemple suivant ajoute `class="pod"` aux frères suivants entre `class="item"` et `class="last"`.

```js
$('.item').nextUntil('.last').addClass('pod');
```

## Méthode .prev()

**API :** http://api.jquery.com/prev/

La méthode `.prev()` retourne le frère prédédent l'élément sélectionné.

L'exemple suivant ajoute `class="pod"` au frère prédédent de `class="item"`.

```js
$('.item').prev().addClass('pod');
```

## Méthode .prevAll()

**API :** http://api.jquery.com/prevAll/

La méthode `.prevAll()` retourne tous les frères prédédents de l'élément sélectionné.

L'exemple suivant ajoute `class="pod"` aux frères prédédents de `class="item"`.

```js
$('.item').prevAll().addClass('pod');
```

## Méthode .prevUntil()

**API :** http://api.jquery.com/prevUntil/

La méthode `.prevUntil()` retourne tous les frères prédédents entre les éléments sélectionnés.

L'exemple suivant ajoute `class="pod"` aux frères prédédents entre `class="item"` et `class="last"`.

```js
$('.item').prevUntil('.last').addClass('pod');
```
