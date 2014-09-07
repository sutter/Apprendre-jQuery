# La méthode .load()

**API :** http://api.jquery.com/load/

La méthode `.load()` va nous permettre de récupérer du contenu à insérer dans notre page.
Nous pouvons charger des fichiers du type : HTML, PHP, TXT, XML et JSON.

Elle est un raccourci de la fonction `.ajax()`.

## La méthode en détail

```js
$(selecteur).load(url,data,function(reponse,status,xhr)));
```

| Paramètre | Description |
| -- | -- |
| **url** | **Requis**<br/>Une chaîne contenant l'URL vers laquelle la demande est envoyée |
| **data** | **Optionnel**<br/> Spécifie les données à envoyer vers le serveur en même temps que la demande |
| **function(reponse,status,xhr)** | **Optionnel**<br/> Indique une fonction à exécuter la méthode est terminé<br/>Paramètres suepplémentaires : <br/>**- data** - contient les données résultant de la demande <br/> **- status** - contient l'état de la demande ("success", "notmodified", "error", "timeout", ou "parsererror")<br/> **- xhr** - contient l'objet XMLHttpRequest |

## Exemples

### Charger un document

Voici un exemple simple, pour comprendre le fonctionnement.

```js
$('#result').load('result.txt');
```

Nous avons chargé le contenu du ficher *result.txt* dans la balise **#result**.

Faisons de même avec un fichier PHP, mais cette fois si au clic.

```js
$('#a').click(function(){
    $('#result').load('inc/result.php');
});
```

Bien sûr nous pouvons ajouter des effets de fondu.
La méthode consiste à cacher le contenu, le charger puis faire le fondu en *callback*.

```js
$('#a').on('click', function(){
	var box = $('#result');
	box.hide().load('inc/result.php', function() {
		box.fadeIn('750');
	});
});
```

### Charger une partie d'un document

Allons encore plus loin et chargeons une seule partie du fichier suivant.

```html
<div id="box-1">
    <h2>Titre numéro 1</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nam, magnam, repellat dicta nesciunt aperiam cupiditate eligendi incidunt expedita architecto! Modi, praesentium, atque aliquam rem aspernatur id similique doloribus deleniti dolorem.</p>
</div>

<div id="box-2">
    <h2>Titre numéro 2</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
</div>
```

Voici le script pour charger **#box-2** dans **result** au clic sur **#a**.

```js
$('#a').click(function(){
    $('#result').load('inc/result.php #box-2');
});
```

### Passer des paramètres à un fichier PHP

Il nous est possible de demander en PHP à la base de données de nous retournée des informations necessitant un paramètre.

Dans l'exemple ci-dessous, nous récupérons la valeur d'un champ **#search**, puis nous la passons en paramètre.

```js
$('#a').click(function(){
    var param = 'id=' + $('#search').val();
    $('#result').load('inc/result.php', param);
});
```



































