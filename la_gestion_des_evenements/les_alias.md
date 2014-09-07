# Les méthodes d'événements

**API :** http://api.jquery.com/category/events/

L'association d'un gestionnaire à un événement peut aussi s'écrire de façon plus simple.

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

Voici quelques une des méthodes plus utilisées.

## Les événements de la souris

| Événement | Description |
| -- | -- |
| `.click()` | Lors du clic sur l'élément |
| `.dblclick()` | Au double-clic sur l'élément |
| `.scroll()` | Lors du scroll sur l'élément |
| `.mousedown()` | Lorsque le bouton de la souris est enfoncé sur l'élément |
| `.mouseup()` | Lorsque le bouton de la souris est relâché au dessus de l'élément |
| `.mousemove()` | Le pointer se déplace dans l'élément |
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
| `.focus()` | Lorsque l'élément à le focus |
| `.load()` | Lorsque l'élément est chargé |
| `.resize()` | Lorsque l'élément est redimensionné |
| `.change()` | Lorsque l'élément subit un changement |
| `.select()` | Lorsque le texte est sélectionné dans un formulaire |
| `.submit()` | Lorsque le formulaire est soumis |
