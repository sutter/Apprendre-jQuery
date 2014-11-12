# Parcourir les descendants

Dans cette partie, nous verrons les méthodes `children()` et `.find()`.

## Méthode .children()

**API :** http://api.jquery.com/children/

La méthode `.children()` retourne tous les enfants directs de l'élément sélectionné.
Cette méthode ne traverse qu'un seul niveau dans l'arbre DOM.

L'exemple suivant ajoute `class="box-inner"` aux enfants directs de `class="box"`.

```html
<main>
    <section>
        <div class="box">
            <div>
                <div>…</div>
            </div>
        </div>
    </section>
</main>
```

```js
$('.box').children().addClass('box-inner');
```

**Résultat**

```html
<main>
    <section>
        <div class="box">
            <div class="box-inner">
                <div>…</div>
            </div>
        </div>
    </section>
</main>
```

## Méthode .find()

**API :** http://api.jquery.com/find/

La méthode `.find()` retourne tous les enfants passés en paramètre.

L'exemple suivant ajoute `class="is-fixed"` à `id="header"` puis cherche l'enfant `nav` et lui ajoute  `class="parent-is-fixed"`.

```html
<div id="header">
	<header>
		<h1><a href="index.html" class="logo">Logotype</a></h1>
	</header>
	<nav>
		<ul>
			<li>…</li>
		</ul>
	</nav>
</div>
```

```js
$('#header').addClass('is-fixed').find('nav').addClass('parent-is-fixed');
```

**Résultat**

```html
<div id="header" class="is-fixed">
	<header>
		<h1><a href="index.html" class="logo">Logotype</a></h1>
	</header>
	<nav class="parent-is-fixed">
		<ul>
			<li>…</li>
		</ul>
	</nav>
</div>
```
