# La méthode .post()

**API :** http://api.jquery.com/jQuery.post/

La méthode `.post()` permet d'envoyer des données.
Par exemple, vous pouvez l'utiliser pour envoyer des données saisies dans un formulaire.

La méthode consiste à envoyer des données vers un fichier *Php* qui lui se chargera de les transmettre. Elle peut même retourner des informations en *callback* dans la page.

```js
$.post('send.php',
    {
        name: 'Jean-Michel',
        email: 'jeanmich@caramail.com'
    }, function(data) {
        alert(data);
});
```

## La méthode en détail

```js
$.get( url, data, function(data,status,xhr), dataType );
```

| Paramètre | Description |
| -- | -- |
| **url** | **Requis**<br/>Une chaîne contenant l'URL vers laquelle la demande est envoyée |
| **data** | **Optionnel**<br/> Spécifie les données à envoyer vers le serveur en même temps que la demande |
| **function(data,status,xhr)** | **Optionnel**<br/> Indique une fonction à exécuter la méthode est terminée<br/>Paramètres supplémentaires : <br/>**- data** - contient les données résultant de la demande <br/> **- status** - contient l'état de la demande ("success", "notmodified", "error", "timeout", ou "parsererror")<br/> **- xhr** - contient l'objet XMLHttpRequest |
| **dataType** | **Optionnel**<br/>Spécifie le type de données attendu de la réponse du serveur. Par défaut jQuery effectue une estimation automatique (*xml*, *json*, *script*, ou *html*) |

## Exemple d'envoi de données

Dans l'exemple suivant nous envoyons un requête afin de faire une recherche, puis nous affichons le résultat de la recherche.

<small>Cet exemple ne contient pas le fichier PHP de traitement, ce n'est pas le sujet de ce cours.</small>

### La structure **html**
```html
<form action="/" id="searchForm">
    <input type="text" name="s" placeholder="Rechercher…">
    <input type="submit" value="Ok">
</form>
<div id="result"></div>
```

### Le script **jQuery** de traitement
```js
$('#searchForm').submit(function(event) {

  // Stop la propagation par défaut
  event.preventDefault();

  // Récupération des valeurs
  var $form = $(this),
       term = $form.find( "input[name='s']" ).val(),
       url = $form.attr( "action" );

  // Envoie des données
  var posting = $.post( url, { s: term } );

  // Reception des données et affichage
  posting.done(function(data) {
    var content = $(data).find('#content');
    $('#result').empty().append(content);
  });

});
```
