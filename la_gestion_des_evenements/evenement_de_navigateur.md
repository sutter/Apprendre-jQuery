# Les événements de navigateur

**API :** http://api.jquery.com/category/events/browser-events/

jQuery permet d'écouter les événements déclenchés par le navigateur.

| Méthode | Description |
| -- | -- |
| `.resize()` | Au redimensionnement de la fenêtre du navigateur |
| `.scroll()` | Au scroll dans un élément |

## Méthode .resize()

La méthode resize sert à écouter l'événement de redimensionnement du navigateur.

Prenons un exemple plus intrusif, qui nous servira juste à voir le fonctionnement de cette méthode.

```js
$(window).resize(function() {
    alert('Je redimensionne mon navigateur');
});
```

Cette méthode sera bien utile pour adapter certains de vos scripts au responsive webdesign. Par exemple lors du calcul de hauteur de certains éléments. Nous le verrons d'ailleurs dans la partie expliquant la manipulation de dimensions.


## Méthode .scroll()

La méthode `.scroll()` sert à écouter l'événement de scroll dans un élément.

Dans l'exemple suivant, nous ajoutons un message dans la console lors du scroll dans le navigateur.

```js
$(window).scroll(function() {
    console.log('Je scroll dans ma page');
});
```
