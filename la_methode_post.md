# La méthode .post()

**API :** http://api.jquery.com/jQuery.post/

La méthode `.post()` permet d'envoyer des données.
Par exemple, vous pouvez l'utiliser pour envoyer des données saisies dans un formulaire.

La méthode consiste à envoyer des données vers un fichier *Php* qui lui se chargera de les transmettre. Elle peut même retourner des informations en *callback* dans la page.

```js
$.post('send.php',
    {
        name: 'Jean-Michel',
        email: 'jeanmich@gmail.com'
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

Cet exemple ne contient pas le fichier *Php* de traitement, ce n'est pas le sujet de ce cours.

**Attention !**<br/>
Cet exemple n'est pas sécurisé, il n'y a pas de contrôle sur les données envoyées.

### La structure **html**
```html
<form role="form" action="send.php" method="post">
	<div class="form-group">
		<label for="#name">Nom :</label>
		<input type="text" name="name" id="name" required>
	</div>
	<div class="form-group">
		<label for="email">Email :</label>
		<input type="email" name="email" id="email" required>
	</div>
    <input id="submit" type="submit" value="OK">
</form>
<div id="result"></div>
```

### Le script **jQuery** de traitement
```js
$('#submit').click(function() {
    $.post('send.php',
        {
            name: 'Jean-Michel',
            email: 'jeanmich@gmail.com'
        }, function(data) {
            alert(data);
    });
    // Annule comportement par défault
    return false;
});
```
