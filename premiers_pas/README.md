# Premiers pas

Nous avons vu à l'étape précédente comme installer jQuery dans notre projet.
Maintenant, rentrons dans le vif du sujet, l'utilisation de la librairie.

Nous allons créer un nouveau fichier **app.js** contenant un script modifiant une page web.
Par convention nous utiliserons un dossier **js** contenant l'ensemble des scripts du projet.

**Voici le contenu de notre page "index.html" :**

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Permiers pas avec jQuery</title>
</head>
<body>
    <div id="text-html">Texte en HTML</div>
    <div id="text-js"></div>
    <!-- en dessous les scripts JS -->
    <script src="js/jquery-2.1.1.min.js"></script>
    <script src="js/app.js"></script>
</body>
</html>
```

**Voici le contenu de notre script "app.js" :**

```js
$(function() {
    $('#text-js').html('Texte renseigné par le bais de jQuery');
});
```

**Voici le résultat :**
<br/>Nous nous apercevons que le DOM a bien été modifié par jQuery.

<p data-height="140" data-theme-id="7816" data-slug-hash="fDbBv" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/sutterlity/pen/fDbBv/'>Premier pas jQuery</a> by Sutterlity (<a href='http://codepen.io/sutterlity'>@sutterlity</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>
