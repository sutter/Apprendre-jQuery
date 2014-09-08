# Les opérateurs arithmétiques

Les opérateurs de calcul permettent de modifier mathématiquement la valeur d'une variable.

Ils sont à la base de tout calcul et sont au nombre de 5 :

| Opérateurs | Signe | Effet | Exemple | Résultat (avec x valant 7) |
| -- | -- | -- | -- | -- |
| Addition | **+** | Ajoute deux valeurs | x + 3 | 10 |
| Soustraction | **-** | Soustrait deux valeurs | x - 3 | 7 |
| Multiplication | ***** | Multiplie les valeurs | x * 3 | 21 |
| Division | **/** | Divise deux valeurs | x / 3 | 2.3333333 |
| Modulo | **%** | Retourne le reste de la division entière de l'opérant de gauche par celle de droite | x % 2 | 1 |

## Calculs simples

Faire des calculs avec JavaScript s'avère très simple.

```js
var result = 7 + 2;
console.log(result); // Affiche : 9
```

Nous pouvons faire des calculs avec des variables contenant des valeurs de type numérique.

```js
var number_1 = 7, number_2 = 2, result;
result = number_1 + number_2;
console.log(result); // Affiche : 9
```

Nous pouvons faire des calculs plus complexes comprenant plusieurs opérateurs.

```js
var result = (((3 + 4) - 1) / 2) * 3;
console.log(result); // Affiche : 9
```

## Simplification des calculs

Il est fréquent d’écrire ce type de calcul.
```js
var maVariable = 7;
    maVariable = maVariable + 2
console.log(maVariable); // Affiche : 9
```

Il existe une façon plus concise permettant d'éviter la redondance de variables.

```js
var maVariable = 7;
    maVariable += 2;
console.log(maVariable); // Affiche : 9
```

On procèdera de la même manière pour chaque opérateur.

```js
maVariable += 2;
maVariable -= 2;
maVariable *= 2;
maVariable /= 2;
maVariable %= 2;
```
