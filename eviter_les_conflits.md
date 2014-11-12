# Éviter les conflits

**Dans cette partie nous allons voir comment gérer les conflits entre plusieures bibliothèques jQuery.**

Les pluparts des bibliothèques jQuery utilisent le signe `$` comme préfix de sélecteurs d'éléments. Bien entendu, cela a pour effet de produire des conflits.

Jquery à prévu une alternative afin de palier à ce problème avec la méthode `noConflict()`. Il suffira de remplacer `$` par `jQuery`.

```js
jQuery.noConflict();
```

Une fois ce code déclaré, vous pouvez continuer à utiliser `$` pour l'autre bibliothèque.

```html
<script src="js/jquery.js"></script>
<script src="js/mootools.js"></script>
<script>
    jQuery.noConflict();

    // Ici vos codes jQuery avec comme préfixe `jQuery`
    jQuery('.box_inner').addClass('rounded');

    // Pour l'autre bibliothèque `$`
    $('.box').set('opacity',0);
</script>
```
