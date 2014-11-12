# La méthode .ajax()


La méthode `.ajax()` est l'artillerie lourde. Elle permet de maîtriser l'ensemble des paramètres de requête.
Les autres méthodes vues juste avant sont seulement des raccourcis d'`.ajax()`.

Cette méthode peut s'écrire de deux façons:

```js
$.ajax(url, {options});
```
**ou**
```js
$.ajax({options});
```

## Paramétrer sa requête

Voici les options les plus utilisées :

| Option | Description |
| -- | -- |
| **URL** | Adresse à laquelle la requête est envoyée |
| **type** | Le type de requête *GET* (par défaut) ou *$POST* |
| **data** | Les données à envoyer au serveur |
| **datatype** | Le type de données pouvant être transmises au serveur : *php*, *html*, *script*, *json* et *xml* |
| **success** | La fonction à appeler si la requête a abouti |
| **error** | La fonction à appeler si la requête n'a pas abouti |
| **timeout** | Le délai maximum en millisecondes de traitement de la demande. Passé ce délai, elle retourne le paramètre **error**. |

Bien sûr, il existe bien d'autres options que vous pouvez retrouver dans l'[API jQuery](http://api.jquery.com/jQuery.ajax/).


## Chargement de fichier

Voici un exemple simple permettant de comprendre le fonctionnement.

```js
// Au clic sur le bouton #search je lance la fonction
$('#search').on('click', function(){

    // J'initialise le variable box
	var box = $('#result');

	// Je définis ma requête ajax
	$.ajax({

	    // Adresse à laquelle la requête est envoyée
    	url: '../inc/search.php',

    	// Le délai maximun en millisecondes de traitement de la demande
    	timeout: 4000,

    	// La fonction à apeller si la requête aboutie
    	success: function (data) {
    	    // Je charge les données dans box
    		box.html(data);
    	},

    	// La fonction à appeler si la requête n'a pas abouti
    	error: function() {
    	    // J'affiche un message d'erreur
    		box.html("Désolé, aucun résultat trouvé.").;
    	}

    });

});
```
