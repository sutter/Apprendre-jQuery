# Parcourir les ancêtres

Dans cette partie nous verrons les méthodes `parent()`,`.parents()`, `.parentUntill()` et `.closest()`.

## Méthode .parent()

**API :** http://api.jquery.com/parent/

La méthode `.parent()` retourne l'élément parent direct de l'élément sélectionné.
Cette méthode ne traverse qu'un seul niveau dans l'arborescence DOM.

L'exemple suivant retourne l'élément parent direct de chaque `class="box-inner"` et lui ajoute `class="box"`.

```html
<main>
    <section>
        <div>
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

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

La méthode `.parents()` retourne tous les éléments ancêtres de l'élément sélectionné.

L'exemple suivant retourne les éléments parents jusqu'à `main` et leur ajoute `class="clearfix"`.

```html
<main>
    <section>
        <div>
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

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

```html
<main>
    <section>
        <div>
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

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

## Méthode .closest()

**API :** http://api.jquery.com/closest/

La méthode `.closest()` retourne le plus proche élément ancêtre de l'élément sélectionné.

L'exemple suivant retourne le plus proche élément ancêtre `section` et lui ajoute `class="clearfix"`.

```html
<main>
    <section>
        <div>
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```

```js
$('.box-inner').closest('section').addClass('clearfix');
```

**Résultat**

```html
<main>
    <section class="clearfix">
        <div>
            <div class="box-inner">…</div>
        </div>
    </section>
</main>
```
