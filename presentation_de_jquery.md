# Présentation de jQuery

jQuery est une bibliothèque JavaScript libre et multi-plateforme créée pour faciliter l'écriture de scripts côté client dans le code HTML. La première version est lancée en janvier 2006 par John Resig (un petit génie du JavaScript).

La bibliothèque contient notamment les fonctionnalités suivantes :

* Parcours et modifications du DOM ;
* Gestion des événements ;
* Effets visuels et animations ;
* Manipulation des CSS ;
* Ajax ;
* Plugins ;
* Utilitaires

Pour vous faire un rapide comparatif d'écriture, voici des exemples comparant jQuery à JavaScript.

** Évènements **
```js
// jQuery
$(document).ready(function() {
    // vos scripts
})

// Javascript
document.addEventListener('DOMContentLoaded', function() {
    // vos scripts
})
```

```js
// jQuery
$('a').click(function() {
  // vos scripts
})

// Javascript
[].forEach.call(document.querySelectorAll('a'), function(el) {
    el.addEventListener('click', function() {
        // vos scripts
    })
})
```

** Sélecteurs **

```js
// jQuery
var divs = $('div')

// Javascript
var divs = document.querySelectorAll('div')
```

*Extrait de code issu de l'article : http://putaindecode.fr/posts/js/de-jquery-a-vanillajs/*
