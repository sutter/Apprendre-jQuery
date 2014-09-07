# La gestion des événements

En JavaScript, nous travaillons en permanence avec des événements comme le clic, une touche une clavier pressée, le chargement d'un élément…

jQuery nous propose une gestion des événements au travers de différentes méthodes.
Elles sont utilisées pour enregistrer les comportements lorsque l'utilisateur interagit avec le navigateur, et servent à manipuler les comportements enregistrés.

**Liste des méthodes d'événements :** http://api.jquery.com/category/events/


## Effectuer une tâche au chargement d'une page

Prenons l'exemple d'un événement que vous connaissez déjà :

```js
// Quand le DOM est prêt, nous appelons tous nos scripts
$(document).ready(function() {
    // Ici le DOM est prêt, appelons nos scripts
});
```

Cette fonction utilise avec la méthode `.ready()` qui écoute le chargement de la page.

L'écoute d'événement consiste à attacher une action à remplir à un élément pour déclencher une fonction que nous appellerons **écouteur d'événement**.


Cette fonction est la solution jQuery pour effectuer les tâches JavaScript déclenchées par l'événement `onload`.
Les résultats sont équivalents, mais ne sont pas exécutés au même moment.

L'événement `onload` est effectué quand le DOM est entièrement chargé (les images, etc), tandis que la méthode `.ready()` écoute juste le fait que le DOM est prêt (entièrement lu).

Si nous voulons écouter le chargement entier du DOM nous utiliserons la fonction suivante.

```js
$(window).on("load", function(){
    // Ici le DOM est entièrement chargé, appelons nos scripts
});
```
