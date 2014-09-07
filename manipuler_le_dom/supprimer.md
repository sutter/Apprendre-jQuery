# Supprimer du contenu

Dans cette partie, nous verrons les méthodes `.remove()` et `.empty()`.

## Méthode .remove()

**API :** http://api.jquery.com/remove/

La méthode `.remove()` supprime du DOM l'élément sélectionné.

L'exemple suivant supprime du DOM `class="box"`.

```js
$('.box').remove();
```

**Résultat**

Avant le script :

```html
<div id="main">
    <div class="other">Je suis ingénieur informaticien</div>
    <div class="box">Je suis magicien</div>
</di>
```
Après le script :

```html
<div id="main">
    <div class="other">Je suis ingénieur informaticien</div>
</di>
```

## Méthode .empty()

**API :** http://api.jquery.com/empty/

La méthode `.empty()` vide le contenu de l'élément sélectionné.

L'exemple suivant vide le contenu de l'élément `class="box"`.

```js
$('.box').empty();
```

**Résultat**

Avant le script :

```html
<div id="main">
    <div class="other">Je suis ingénieur informaticien</div>
    <div class="box">Je suis magicien</div>
</di>
```
Après le script :

```html
<div id="main">
    <div class="other">Je suis ingénieur informaticien</div>
    <div class="box"></div>
</di>
```