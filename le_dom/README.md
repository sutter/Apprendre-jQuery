# Le DOM

Le DOM ou **Document Object Model** est un standard du W3C qui définit l'arborescence du document HTML.

jQuery est utilisé pour manipuler le DOM en écriture et en lecture.

Prenons le cas où le DOM n'est pas encore totalement construit lors du chargement de la page et que le script jQuery est exécuté ; les sripts produiront des erreurs.

Pour attendre que le DOM soit entièrement chargé et ainsi éviter des erreurs.

**Version JavaScript**

```js
document.addEventListener('DOMContentLoaded', function() {
  // Ici le DOM est prêt
})
```

**Version jQuery**

Avec jQuery, nous utiliserons la méthode `.ready()` prévue à cet effet.

```js
jQuery(document).ready(function() {
    // Ici le DOM est prêt
});
```

Cette écriture jQuery peut être simplifiée par l'alias JavaScript `$`:

```js
$(document).ready(function() {
    // Ici le DOM est prêt
});
```

Afin d'être encore plus concis le `$(document).ready` peut être omis :

```js
$(function() {
    // Ici le DOM est prêt
});
```

**Ces 3 instructions sont équivalentes**, mais ma préférence va à la troisième solution beaucoup plus facile à retenir.
