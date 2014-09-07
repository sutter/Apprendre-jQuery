# Manipuler le texte

Dans cette partie nous verrons les méthodes `.text()`,`.html()` et `.val()`.

## Méthode .text()

**API :** http://api.jquery.com/text/

La méthode `.text()` récupère ou remplace le contenu en texte brut, sans prendre en sans prendre en compte les balises HTML.

L'exemple suivant remplace le contenu texte de la balise `class="box"`.

```js
$('.box').text('Hello world');
```

L'exemple suivant récupère le texte de `class="box"` et l'affiche dans la console du navigateur.

```js
console.log( $('.box').text() );
```

## Méthode .html()

**API :** http://api.jquery.com/html/

La méthode `.html()` récupère ou remplace le contenu HTML de l'élément.

L'exemple suivant remplace le contenu HTML de la balise `class="box"`.

```js
$('.box').html('<h1>Hello world</h1>');
```

L'exemple suivant récupère le contenu HTML de `class="box"` et l'affiche dans la console du navigateur.

```js
console.log( $('.box').html() );
```

## Méthode .val()

**API :** http://api.jquery.com/val/

La méthode `.val()` récupère ou remplace la value d'un élément de formulaire *input text*, *textarea* etc. Dans les champs de type *radio* et *checked* elle renvoie **:checked** ou pas.

Dans l'exemple suivant nous affichons la valeur du champ `#name`dans une boite d'alerte lors du click sur `#submit`.

```js
$('#submit').click(function(){
    alert($('#name').val());
});
```
