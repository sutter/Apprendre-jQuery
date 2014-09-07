# Les types

## Les chaînes de caractères

Ce type représente n’importe quel texte.
On peut l'assigner de deux façons différentes.

**Avec des guillemets**
```js
maVariable = "J'aime JavaScript";
```

**Avec des apostrophes**

```js
maVariable = 'J\'aime JavaScript';
```

**Attention**, si vous voulez des apostrophes pour déclarer votre variable et que vous utilisez des apostrophes dans le texte vous devez échapper des derniers avec le caractère `\` (antislash).
Sinon JavaScript croira que le code s’arrêtera à la première apostrophe, et produira une erreur.

## Le type numérique

Ce type de variable représente tout nombre, que ce soit un entier, un négatif, un nombre scientifique, etc.

```js
maVariable = 3;
```

Un chiffre décimal se déclare avec un point comme séparateur et non une virgule.
```js
maVariable = 3.5;
```

**Attention**, si vous écrivez le nombre entre des guillemets ou des apostrophes il sera reconnu comme une chaîne de caractères.
```js
maVariable = '3'; // Chaîne de caractères
```

## Les booléens

Désigne un paramètre qui peut avoir comme valeur **true** ou **false**.

Lorsqu'aucune valeur n'est passée, ou la valeur 0, ou une chaîne de caractères vide, ou null, ou undefined ou bien NaN, la valeur de l'objet est initialisée à `False`.<br/>Dans tous les autres cas, l'objet Boolean possédera la valeur `True`.

Ces deux états s'écrivent de la façon suivante :

```js
var isTrue = true;
var isFalse = false;
```

## Test de type

Nous pouvons vérifier le type de variable avec l’instruction **typeof**.

La fonction **console.log()** affiche le résultat dans la [console](http://www.alsacreations.com/astuce/lire/1436-console-javascript.html) du navigateur.

```js
var myVariable = 2;
console.log(typeof myVariable); // Affiche : « number »

var myVariable = 'Mon texte';
console.log(typeof myVariable); // Affiche : « string »

var myVariable = false;
console.log(typeof myVariable); // Affiche : « boolean »
```

Nous pouvons tester l’existence de variable avec la même instruction.

```js
console.log(typeof otherVariable); // Affiche : « undefined »
```
