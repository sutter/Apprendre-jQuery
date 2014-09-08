# La propagation d'événements

Lorsque que vous déclarez un événement il se propage à travers le DOM jusqu'à rencontrer l'élément ciblé.

Prenons le cas d'un élément unique :

```html
<a id="totop" href="#">Haut de page</a>

```

```js
$("#totop").click(function(){
    alert($(this).html());
});
```

L'événement pointe sur un élément unique `id="yolo"` et le script est exécuté une seule fois.

Tandis que dans le cas suivant, le message d'alerte apparaîtra deux fois.

```html
<ul>
    <li>Niveau 1</li>
    <li>Niveau 1</li>
    <li>
        <ul>
            <li>Niveau 2</li>
            <li>Niveau 2</li>
        </ul>
    </li>
    <li>Niveau 1</li>
    <li>Niveau 1</li>
</ul>
```

```js
$("li").click(function(){
    alert($(this).html());
});
```


L'événement se propagera à travers tout les **li** du document suivant le **principe de bouillonnement**.
Le script sera exécuté à chaque élément **li** rencontré, peu importe son niveau dans le DOM.
C'est-ce que l'ont appelle la propagation d'événements.

## Éviter la propagation

Dans certains cas la propagation est problématique, heureusement jQuery propose deux moyens de les éviter.

### event.stopPropagation()

**API :** http://api.jquery.com/event.stoppropagation/

`event.stopPropagation()` empêche l'évènement de se propager dans l'arbre DOM en évitant le bouillonnement.
Dans l'exemple ci-dessous, le message d'alerte n'apparaît qu'une fois.

```js
$("li").click(function(e){
    event.stopPropagation();
    alert($(this).html());
});
```

### return false

`return false` empêche-lui aussi l'évènement de se propager dans l'arbre DOM en évitant le bouillonnement comme `event.stopPropagation()`, mais il annule aussi l'action en cours.

Dans l'exemple suivant nous affichons un message d'alerte et nous empêchons de mofidier l'URL au clic sur une l'ancre.

```html
<a id="totop" href="#">Haut de page</a>

```

```js
$("#totop").click(function(){
    alert($(this).html());
    return false
});
```

**Attention**<br/>
Les déclarations en dessous de `return false` ne sont pas traitées.







