# Le DOM

Le DOM ou **Document Object Model** est un standard du W3C qui définit l'arborescence du document HTML.

jQuery est utilisé pour manipuler le DOM en écriture et en lecture.

Prenons le cas ou le DOM n'est pas encore totalement construit lors du chargement de la page et que le script jQuery est exécuté. Nous nous retrouverons avec des erreurs.

Afin d'éviter ces erreurs et attendre que le DOM soit entièrement chargé, nous utiliserons la méthode `.ready()`.

```js
$(document).ready(function() {
    // Ici le DOM est prêt
});
```

Cette écriture jQuery peut être simplifiée par l'alias JavaScript `$`:

```js
$(document).ready(function() {
    // Ici le DOM est prêt
});
```

Afin d'être encore plus concis le "(document).ready" peut être omis :

```js
$(function() {
    // Ici le DOM est prêt
});
```

**Ces 3 instructions sont équivalentes**, mais ma préférence va à la troisième solution beaucoup plus facile à retenir.
