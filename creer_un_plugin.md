# Créer un plugin

Dans cette partie nous allons voir comment créer son propre plugin jQuery.

Rien de compliqué, il suffit de déclarer le plugin, puis de l'appeler.

**Déclarer un plugin**

```js
(function($) {
    $.fn.nomDuPlugin = function(parametre, …) {
        // Ici vos scripts
    };
})(jQuery);
```

**Appeler un plugin**

```js
$('#elem').nomDuPlugin(58);
```

Bien entendu, notre plugin peut prendre :
* aucun paramètre ;
* un paramètre ;
* plusieurs paramètres.


## Exemple de plugin sans paramètre

Dans cet exemple nous allons créer un plugin nous permettant d'ajouter un attribut `target="_blank"` aux éléments ayant un un attribut `rel="external"`.

**Création du plugin**

```js
(function($) {
    $.fn.newWindow = function() {
        $(this).attr('target', '_blank');
    };
})(jQuery);
```

**Appel du plugin**

```js
$('a[rel="external"]').newWindow();
```

## Exemple de plugin avec paramètres

Dans cet exemple nous allons créer un plugin permettant d'ajouter les propriétés CSS `color` et `background-color` avec des valeurs par défaut à un élément.

**Création du plugin**

```js
(function($) {
    $.fn.myPlugin = function( options ) {

        // Déclarations de valeurs par défaut
        var settings = $.extend({
            color           : '#09f',
            backgroundColor : "#f90"
        }, options );

        // Application des valeurs 'par défaut si non renseignées'
        return this.css({
            color           : settings.color,
            backgroundColor : settings.backgroundColor
        });

    };
})(jQuery);
```

**Appel du plugin**

```js
$('.box').myPlugin({color: 'orange'});
```
