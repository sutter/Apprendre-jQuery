# Parcourir les ancêtres

Dans cette partie nous verrons les méthodes `parent()`,`.parents()` et `.parentUntill()`.

## Méthode .parent()

**API :** http://api.jquery.com/parent/

La méthode `.parent()` retourne l'élément parent direct de l'élément sélectionné.
Cette méthode ne traverse qu'un seul niveau dans l'arborescence DOM.

L'exemple suivant retourne l'élément parent direct de chaque `class="box-inner"` et lui ajoute `class="box"`.

```js
$('.box-inner').parent().addClass('box');
```

**Résultat**

```html
<main>
    <section>
        <div class="box">
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

## Méthode .parents()

**API :** http://api.jquery.com/parents/

La méthode `.parents()` retourne tous les éléments de l'élément sélectionné.

L'exemple suivant retourne les éléments parents jusqu'à `main` et leur ajoute `class="clearfix"`.

```js
$('.box-inner').parents('main').addClass('clearfix');
```

**Résultat**

```html
<main class="clearfix">
    <section class="clearfix">
        <div class="clearfix">
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

## Méthode .parentsUntil()

**API :** http://api.jquery.com/parentsUntil/

La méthode `.parentsUntil()` retourne tous les éléments ancêtres entre deux arguments donnés.

L'exemple suivant retourne les éléments parents au niveau en dessous de `main` et leur ajoute `class="clearfix"`.

```js
$('.box-inner').parentsUntil('main').addClass('clearfix');
```

**Résultat**

```html
<main>
    <section class="clearfix">
        <div class="clearfix">
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```
