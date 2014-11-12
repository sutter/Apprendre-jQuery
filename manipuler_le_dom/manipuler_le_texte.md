# Manipuler le texte

Dans cette partie, nous verrons les méthodes `.text()`,`.html()` et `.val()`.

## Méthode .text()

**API :** http://api.jquery.com/text/

La méthode `.text()` récupère ou remplace le contenu en texte brut sans prendre en compte les balises HTML.

L'exemple suivant remplace le contenu texte de la balise `class="box"`.

```html
<div class="box">Je suis magicien</div>
```

```js
$('.box').text('Hello world');
```

**Résultat**

```html
<div class="box">Hello world</div>
```

## Méthode .html()

**API :** http://api.jquery.com/html/

La méthode `.html()` récupère ou remplace le contenu HTML de l'élément.

L'exemple suivant remplace le contenu HTML de la balise `class="box"`.

```html
<div class="box">Je suis magicien</div>
```

```js
$('.box').html('<h1>Hello world</h1>');
```

**Résultat**

```html
<div class="box">
    <h1>Hello world</h1>
</div>
```

## Méthode .val()

**API :** http://api.jquery.com/val/

La méthode `.val()` récupère ou remplace la value d'un élément de formulaire *input text*, *textarea* etc. Dans les champs de type *radio* et *checked* elle renvoie **:checked** ou pas.

Dans l'exemple suivant, nous affichons la valeur du champ `#name`dans une boite d'alerte lors du click sur `#submit`.

```html
<form role="form" action="#" class="box">
    <div class="form-group">
        <label for="#name">Nom :</label>
        <input type="text" name="name" id="name">
    </div>
    <input id="submit" class="btn btn-primary" type="submit" value="Envoyer">
</form>
```

```js
$('#submit').click(function(){
    alert($('#name').val());
});
```

<p data-height="136" data-theme-id="7816" data-slug-hash="KwKPNR" data-default-tab="result" data-user="sutterlity" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/KwKPNR/'>.val()</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
