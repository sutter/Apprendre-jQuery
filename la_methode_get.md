# La méthode .get()

**API :** http://api.jquery.com/jQuery.get/

La méthode `.get()` permet de recevoir des données.
Contairemement à la méthode `.load()`, elle nous permet non pas de recevoir du contenu directement dans l'élément ciblé, mais de nous laisser le choix sur les actions à faire.


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

## Exemples

### Charger un document

Prenons l'exemple suivant, le fichier **'inc/test.html'** se charge dans **#result**.

```js
$.get('inc/test.html', function( data ) {
    $('#result').html( data );
});
```

Elle est un raccourci de la fonction `.ajax()` suivante, que nous verrons dans la prochaine partie.

```js
$.ajax({
    url: 'inc/test.html',
    success: function (data) {
    	$('#result').html( data );
    }
});
```

Maintenant, affichons le statut dans la console.

```js
$.get('inc/test.html', function( data, status ) {
    $('#result').html( data );
    console.log(status);
});
```

### Charger des données de type json

Voici un exemple de chargement de données issues du fichier *json*.

```js
$.get('inc/user.json', function( data ) {
	$('#result').html( data.name + ' : ' +  data.email );
}, 'json');
```
