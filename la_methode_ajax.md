# La méthode .ajax()


La méthode `.ajax()` est l'artillerie lourde, elle nous permet de tout maîtriser.
Les autres méthodes vu juste avant, sont justes des raccourcis d'`.ajax()`.

Cette méthode peut s'écrire de deux façons:

```js
$.ajax(url, {options});
```
**ou**
```js
$.ajax({options});
```

## Paramétrer sa requête

Voici les options les plus utilisées.

| Option | Description |
| -- | -- |
| **URL** | Adresse à laquelle la requête est envoyée |
| **type** | Le type de requête *GET* (par défaut) ou *$POST* |
| **data** | Les données à envoyer au serveur |
| **datatype** | Le type de données qui peut être transmise au serveur : *php*, *html*, *script*, *json* et *xml* |
| **success** | La fonction à apeller si la requête aboutie |
| **error** | La fonction à apeller si la requête n'a pas aboutie |
| **timeout** | Le délai maximum en millisecondes de traitement de la demande. Passé ce délai, elle retourne le paramètre **error**. |

Bien sûr, il existe bien d'autres options que vous pouvez retrouver dans l'[API jQuery](http://api.jquery.com/jQuery.ajax/).

Voici un exemple de requête avec un message en cas d'erreur.

## Chargement de fichier

Voici un exemple simple, pour comprendre le fonctionnement.

```js
// Au clic sur le bouton #search je lance la fonction
$('#search').on('click', function(){

    // J'initialise le variable box
	var box = $('#result');

	// Je défini ma requête ajax
	$.ajax({

	    // Adresse à laquelle la requête est envoyée
    	url: '../inc/search.php',

    	// Le type de donnée
    	dataType : 'php',

    	// Le délai maximun en millisecondes de traitement de la demande
    	timeout: 4000,

    	// La fonction à apeller si la requête aboutie
    	success: function (data) {
    	    // Je charge les données dans box
    		box.html(data);
    	},

    	// La fonction à apeller si la requête n'a pas aboutie
    	error: function() {
    	    // J'affiche un message d'erreur
    		box.html("Désolé, aucun résultat trouvé.").;
    	}

    });

});
```
