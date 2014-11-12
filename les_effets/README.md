# Les effets

**API :** http://api.jquery.com/category/effects/

Dans ce chapitre nous aborderons les effets ainsi que les animations avec jQuery. Nous allons voir comment afficher et cacher des éléments, faire des fondus, des effets de slide ainsi que des animations personnalisées.

## Animation jQuery Vs CSS3

Avant toute chose, j'aimerais faire un point sur la pertinence des effets d'animation jQuery à l'heure du CSS3.

### Animation CSS3

Comme dans cette [démonstration](http://www.justinaguilar.com/animations/) nous pouvons nous rendre compte que les animations CSS3 sont assez puissantes. Elles sont aussi plus rapides car intégrées directement dans le navigateur.

L'inconvénient des animations CSS3 réside dans le manque de compatibilité avec les navigateurs anciens (IE8 etc) même si elles ont un *fallback*. En effet, si le navigateur ne les comprend pas, il affiche directement le résultat final laissant ainsi le site fonctionnel.

Lorsque trop d'animations CSS3 sont lancées en même temps, elles ne sont pas fluides.

Il est aussi à l'heure actuelle impossible d'ajouter un *callback* en fin d'animation CSS3, au moins tant que  [transitionend](https://developer.mozilla.org/en-US/docs/Web/Events/transitionend) n'est pas complètement implémenté.


### Animation jQuery

L'avantage majeur des animations jQuery est l'intercompatibilité des navigateurs même IE7 est en mesure de lire une animation jQuery. Bien sûr, nous pouvons aussi ajouter des *callback*.

Lorsqu'il y a beaucoup d'animations, jQuery reste fluide contrairement à CSS3, évitant ainsi les bugs et les artefacts visuels.

Je profite aussi de ce point pour vous parler de la librairie  [Velocity.js](http://julian.com/research/velocity/). Elle propose de remplacer les animations jQuery par une version plus optimisée. Elles sont même plus rapides que les animations CSS3.


### Conclusion

Les animations CSS3 sont plus simples à mettre en place mais souffrent encore de quelques lacunes. Si vous avez besoin de *fallback* il faudra passer par jQuery.

Les animations jQuery sont plus complexes à mettre en place et nécessitent l'import de la librairie. En prenant en compte [Velocity.js](http://julian.com/research/velocity/) elles sont aussi plus performantes.



