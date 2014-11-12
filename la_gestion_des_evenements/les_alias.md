# Les méthodes d'événements

**API :** http://api.jquery.com/category/events/

L'association d'un gestionnaire à un événement peut aussi s'écrire de façon plus simple mais perd l'avantage d'écouter en permanence la page.
Par exemple, si un bouton est créé à l'aide d'un script après que le DOM soit chargé, la méthode `.click()` ne fonctionnera pas.


```js
$('.btn').on('click', function() {
    alert( $(this).text() );
});
```

Devient :

```js
$('.btn').click(function() {
    alert( $(this).text() );
});
```
L'avantage de ces méthodes raccourcies et d'être moins gourmandes en mémoire puisque le DOM n'est pas écouté en permanance.

L'exemple suivant nous permet de montrer que la méthode `.click()`ne fonctionne pas sur le bouton créé après le chargement du DOM.

```html
<div class="box">
  <p>
    <button class="btn btn-primary" id="add">Ajouter un bouton</button>
  </p>
  <p id="container" class="bg-muted">
    <button class="btn btn-default btn-sm">Bouton créer avant le chargement du DOM</button>
  </p>
</div>
```

```js
$('#add').click(function() {
    var html = '<button class="btn btn-default btn-sm">Bouton créer après le chargement du DOM</button>';
    $("button.btn:last").parent().append(html);
});

$("#container .btn").click(function() {
    alert('Méthode .click()');
});

$("#container").on('click', '.btn', function() {
    alert('Méthode .on()');
});
```

<p data-height="136" data-theme-id="7816" data-slug-hash="BDfAd" data-default-tab="result" data-user="sutterlity" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/BDfAd/'>.click() vs .on()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

---

Voici quelques unes des méthodes les plus utilisées.

## Les événements de la souris

| Événement | Description |
| -- | -- |
| `.click()` | Lors du clic sur l'élément |
| `.dblclick()` | Au double-clic sur l'élément |
| `.scroll()` | Lors du scroll sur l'élément |
| `.mousedown()` | Lorsque le bouton de la souris est enfoncé sur l'élément |
| `.mouseup()` | Lorsque le bouton de la souris est relâché au dessus de l'élément |
| `.mousemove()` | Le pointeur se déplace dans l'élément |
| `.mouseover()` | Lorsque le curseur entre dans l'élément |
| `.mouseout()` | Lorsque le curseur sort de l'élément |
| `.mouseenter()` | Lorsque le curseur entre dans l'élément, le bouillonnement n'a pas d'effet |
| `.mouseleave()` | Lorsque le curseur sort de l'élément, le bouillonnement n'a pas d'effet |

## Les événements du clavier

| Événement | Description
| -- | -- |
| `.keydown()` | Lorsqu'une touche du clavier est enfoncée |
| `.keypress()` | Lorsqu'une touche du clavier vient d'être enfoncée |
| `.keyup()` | Lorsqu'une touche vient d'être relachée |

## Les autres événements

| Événement | Description |
| -- | -- |
| `.blur()` | Lorsque l'élément perd son focus |
| `.focus()` | Lorsque l'élément a le focus |
| `.load()` | Lorsque l'élément est chargé |
| `.resize()` | Lorsque l'élément est redimensionné |
| `.change()` | Lorsque l'élément subit un changement |
| `.select()` | Lorsque le texte est sélectionné dans un formulaire |
| `.submit()` | Lorsque le formulaire est soumis |
