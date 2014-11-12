# Parcourir le DOM

**API :** http://api.jquery.com/category/traversing/

Même si les sélecteurs jQuery nous permettent de sélectionner des éléments, nos possibilités sont relativement limitées. jQuery nous propose plusieurs méthodes afin de parcourir le DOM et de faire des tris.

Dans l'exemple ci-dessous, nous ajouterons une classe `.first-level` à l'enfant `ul` de `#menu`.

```js
$('#menu').children('ul').addClass('first-level');
```

Bien sûr nous ne verrons pas toutes les méthodes en détail, mais voici un tableau récapitulatif.

| Méthode | Description |
| -- | -- |
| [`.add()`](http://api.jquery.com/add/) | Ajoute des éléments au sélecteur actuel |
| [`.addBack()`](http://api.jquery.com/addBack/) | Ajoute les précédents éléments sélectionnés au sélecteur actuel|
| [`.children()`](http://api.jquery.com/children) |  Retourne tous les enfants directs de l'élément sélectionné |
| [`.closest()`](http://api.jquery.com/closest/) |  Retourne le plus proche élément ancêtre de l'élément sélectionné |
| [`.contents()`](http://api.jquery.com/contents/) | Les noeuds enfants (y compris les noeuds de texte) |
| [`.each()`](http://api.jquery.com/each/) | Exécute une fonction à chaque élément identifié |
| [`.end()`](http://api.jquery.com/end/) | Termine le filtrage en cours et retourne aux éléments sélectionnés précédemment |
| [`.eq()`](http://api.jquery.com/eq/) | Retourne un élément avec un numéro d'index spécifique des éléments sélectionnés (commence à 0) |
| [`.filter()`](http://api.jquery.com/filter/) | Filtre les éléments qui correspondent au sélecteur indiqué |
| [`.find()`](http://api.jquery.com/find/) | Recherche les éléments enfants qui correspondent au sélecteur |
| [`.first()`](http://api.jquery.com/first/) | Retourne le premier élément des éléments sélectionnés |
| [`.has()`](http://api.jquery.com/has/) | Retourne les éléments ayant à l'intérieur le sélecteur indiqué. |
| [`.is()`](http://api.jquery.com/is/) | Vérifie l'ensemble des éléments sélectionnés contre un sélecteur / élément / objet jQuery, et retourne vrai si au moins un de ces éléments correspond arguments donnés |
| [`.last()`](http://api.jquery.com/last/) | Retourne le dernier élément des éléments sélectionnés |
| [`.map()`](http://api.jquery.com/map/) | Retourne un tableau de valeurs, de l'élément sélectionné |
| [`.next()`](http://api.jquery.com/next/) | Retourne le frère suivant de chaque élément sélectionné, avec filtre (facultatif) |
| [`.nextAll()`](http://api.jquery.com/nextAll/) | Retourne tous les frères suivants de chaque élément sélectionné, avec filtre (facultatif) |
| [`.nextUntil()`](http://api.jquery.com/nextUntil/) | Retourne tous les frères suivants de chaque élément sélectionné entre deux arguments donnés, avec filtre (facultatif) |
| [`.not()`](http://api.jquery.com/not/) | Supprime les éléments qui ne correspondent pas au sélecteur |
| [`.offsetParent()`](http://api.jquery.com/offsetParent/) | Retourne le parent positionné (par exemple de manière relative ou absolue) du 1<sup>er</sup> élément sélectionné. |
| [`.parent()`](http://api.jquery.com/parent/)| Retourne le parent direct, avec filtre (facultatif) |
| [`.parents()`](http://api.jquery.com/parents/) | Retourne tous les éléments ancêtres de l'élément sélectionné |
| [`.parentsUntil()`](http://api.jquery.com/parentsUntil/) | Retourne tous les éléments parents entre deux arguments donnés |
| [`.prev()`](http://api.jquery.com/prev/) | Retourne le frère précédent de chaque élément sélectionné, avec filtre (facultatif) |
| [`.prevAll()`](http://api.jquery.com/prevAll/) | Retourne tous les frères précédents de chaque élément sélectionné, avec filtre (facultatif) |
| [`.prevUntil()`](http://api.jquery.com/prevUntil/) | Retourne tous les frères précédents de chaque élément sélectionné entre deux arguments donnés, avec filtre (facultatif) |
| [`.siblings()`](http://api.jquery.com/siblings/) | Retourne tous les frères, avec filtre (facultatif) |
| [`.slice()`](http://api.jquery.com/slice/) | Retourne les éléments se trouvant dans la plage d’indices indiquée (commence à 0) |
