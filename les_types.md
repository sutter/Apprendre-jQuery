# Les types

## Les chaînes de caractères ou "string"

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

**Attention**, si vous voulez des apostrophes pour déclarer votre variable et que vous utilisez des apostrophes dans le texte vous devez échapper les derniers avec le caractère `\` (antislash).
Dans le cas contraire, JavaScript pensera que le code s’arrête à la première apostrophe et produira une erreur.

## Le type numérique ou "number"

Ce type de variable représente tout nombre  que ce soit un entier, un négatif, un nombre scientifique, etc.

```js
maVariable = 3;
```

Un chiffre décimal se déclare avec un point comme séparateur et non une virgule.
```js
maVariable = 3.5;
```

**Attention**, si vous écrivez le nombre entre guillemets ou avec apostrophes, il sera reconnu comme une chaîne de caractères.
```js
maVariable = '3'; // Chaîne de caractères
```

## Les booléens

Désigne un paramètre qui peut avoir comme valeur **true** ou **false**.

Lorsque :

* aucune valeur n'est passée ;
* la valeur est égale à *0* ;
* une chaîne de caractères est vide, *null*, *undefined* ou *NaN*

la valeur de l'objet est initialisée à `False`.

Dans tous les autres cas, l'objet Boolean possédera la valeur `True`.

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

## La convertion de type

### Convertion type "string" en" number"

Dans certains cas de figure, nous pouvons avoir besoin de convertir une chaîne de caractères en nombre. La méthode `parseInt()` convertie une chaîne de caractères en nombre.

```js
var myVariable = '2',
    n = parseInt(myVariable);
console.log(typeof n); // Affiche : « number »
```

### Convertion type "number" en "string

Pour convertir une chaîne de charactères en nombre, nous pouvons utiliser la méthode`.toString()`.

```js
var myVariable = 2,
    n = myVariable.toString();
console.log(typeof n); // Affiche : « string »
```

















