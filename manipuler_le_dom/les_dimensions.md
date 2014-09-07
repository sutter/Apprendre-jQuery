# Les dimensions

Dans cette partie, nous verrons les méthodes de calcul de dimensions `.width()`, `.innerWidth()`, `.outerWidth()`, `.height()`, `.innerHeight()`, `.outerHeight()`.

Voici le modèle de boite suivant lequel se base les méthodes.

![](../img/img_jquerydim.gif)

| Méthode | Description |
| -- | -- |
| `.width()` | Définis ou retourne la largeur d'un élément.<br/> Les padding, border et les marges ne sont pas compris dans le calcul. |
| `.innerWidth()` | Définis ou retourne la largeur d'un élément.<br/> Les padding sont compris dans le calcul, mais pas les border et les marges. |
| `.outerdWidth()` | Définis ou retourne la largeur d'un élément.<br/> Les padding et les borders sont compris dans le calcul, mais pas les marges. |
| `.outerdWidth(true)` | Définis ou retourne la largeur d'un élément.<br/> Les padding, border et les marges sont compris dans le calcul. |
| `.height()` | Définis ou retourne la hauteur d'un élément.<br/> Les padding, border et les marges ne sont pas compris dans le calcul. |
| `.innerHeight()` | Définis ou retourne la hauteur d'un élément.<br/> Les padding sont compris dans le calcul, mais pas les border et les marges. |
| `.outerdHeight()` | Définis ou retourne la hauteur d'un élément.<br/> Les padding et les borders sont compris dans le calcul, mais pas les marges. |
| `.outerdHeight(true)` | Définis ou retourne la hauteur d'un élément.<br/> Les padding, border et les marges sont compris dans le calcul. |

Voyons maintenant à quoi peuvent maintenant nous servir ces méthodes.

Par exemple, nous pouvons donner la hauteur de la fenêtre aux éléments `<section>`, redimensionnable au resize du navigateur (astuce pour le responsive).

```js
// Création de la fonction
function fullHeight() {
    var hWindow = $(window).height();
    $('section').css('height', hWindow);
}

$(function() {
    // Lancer la fonction quand le DOM est ready
    fullHeight();
});

$(window).resize(function() {
    // Lancer la fonction au redimensionnement de la fenêtre
    fullHeight();
});
```

<p data-height="300" data-theme-id="7816" data-slug-hash="bgops" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/bgops/'>.height()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

Nous pouvons aussi calculer la hauteur d'un élément pour l'assigner à un autre.

```js
// Création de la fonction
function sameHeight(elem) {
    // initialisation de la hauteur de base à 0
    var tallest = 0;
    // Parcours de tous les éléments
    elem.each(function() {
        // Mise en variable de la hauteur de l'élément
        var thisHeight = $(this).height();
        // Condition pour savoir si la hauteur de l'élément est plus grande que 'tallest'
        if(thisHeight > tallest) {
            // Si l'élément est plus grand, nous assignons la nouvelle valeur à 'tallest'
            tallest = thisHeight;
        }
    });
    // Nous appliquons le style CSS sur l'élément
    elem.height(tallest);
}

$(function(){
    // Lancer la fonction quand le DOM est ready
    sameHeight( $('.box-list-item') );
});
```

<p data-height="256" data-theme-id="7816" data-slug-hash="otBkx" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/otBkx/'>.height()-2</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>




