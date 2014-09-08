# Les conditions

On appelle structure conditionnelle les instructions qui permettent de tester si une condition est vraie (true) ou non (false).

En JavaScript les conditions sont constituées de :
* valeurs à tester ;
* un opérateur logique ;
* un opérateur de comparaison (optionnel).

## Les opérateurs de comparaison

| Opérateurs | Désignation | Effet | Exemple | Résultat |
| :--: | -- | -- | :--: | -- |
| **==** | opérateur d'égalité | Compare deux valeurs et vérifie leur égalité | x == 3 | Retourne True si X est égal à 3, sinon False |
| **!=** | opérateur de différence | Vérifie qu'une variable est différente d'une valeur | x != 3 | Retourne 1 si X est différent de 3, sinon 0 |
| ***===*** | opérateur d'identité | Vérifie l'identité de valeur et de type de deux valeurs | a === b | Retourne True si a est égal à b et est de même type, sinon False |
| **!==** | opérateur de non identité | Vérifie la non identité de valeur et de type de deux valeurs, c'est-à-dire si les deux valeurs n'ont pas la même valeur ou bien sont de types différents. | a !== b | Retourne True si a est différent de b ou bien est de type différent, sinon False |
| **>** | opérateur de supériorité stricte | Vérifie qu'une variable est strictement supérieure à une valeur | x > 3 | Retourne True si X est supérieur à 3, sinon False |
|  **>=** | opérateur de supériorité | Vérifie qu'une variable est supérieure ou égale à une valeur | x >= 3 | Retourne True si X est supérieur ou égal à 3, sinon False |
|  **<** | opérateur d'infériorité stricte | Vérifie qu'une variable est strictement inférieure à une valeur | x < 3 | Retourne True si X est inférieur à 3, sinon False |
| **<=** | opérateur d'infériorité | Vérifie qu'une variable est inférieure ou égale à une valeur | x <= 3 | Retourne True si X est inférieur ou égale à 3, sinon False |


## Les opérateurs logiques (booléens)

| Opérateurs | Désignation | Effet | Syntaxe |
| :--: | -- | -- | -- |
| **&#124;&#124;** | OU logique | Vérifie qu'une des conditions est réalisée | ( (expression1) &#124;&#124; (expression2) ) |
| **&&** | ET logique | Vérifie que toutes les conditions sont réalisées | ( (expression1) && (expression2) ) |
| **!** | NON logique | Inverse l'état d'une variable booléenne (retourne la valeur 1 si la variable vaut 0, 0 si elle vaut 1) | ( !condition ) |


## Instruction if

Elle permet d'exécuter une série d'instructions lorsqu'une condition est réalisée.

La syntaxe de cette expression est la suivante.

```js
if ( si condition réalisée ) {
    liste d'instructions
}
```

Il est possible de définir plusieurs conditions à remplir avec les opérateurs `&&` et `||`.

Par exemple, l'instruction ci-dessous teste si les deux conditions sont réalisées.

```js
if ( (condition1) && (condition2) ) { … }
```

L'instruction suivante exécutera les instructions si l'une ou l'autre des deux conditions est réalisée.

```js
if ( (condition1) || (condition2) ) { … }
```

**Exemple**

```js
// Déclaration de variable et assignation de valeur
var monArgent = 1;
var prixCafe  = 1.2;

// Condition
// Si
if ( monArgent >= prixCafe) {
    console.log("J'ai assez d'argent pour boire un café.");
}
```

## Instruction if … else

L'instruction **if** dans sa forme basique permet de tester qu'une condition. Or, la plupart du temps, on aimerait pouvoir choisir les instructions à exécuter lorsque la condition n'est pas remplie.

L'expression **if … else** permet dès lors d'exécuter une autre série d'instructions en cas de non-réalisation de la condition.

La syntaxe de cette expression est la suivante :

```js
if ( si condition réalisée ) {
    // liste d'instructions
}
else {
    // sinon autre série d'instructions
}
```

**Remarque :**<br/>
Les structures conditionnelles pouvant être imbriquées, il peut être utile d'indenter le code pour plus de lisibilité. En d'autres termes, il s'agit de décaler à l'aide d'une tabulation chaque bloc d'instructions pour pouvoir rapidement visualiser l'imbrication des structures.

**Exemple**

```js
// Déclaration de variable et assignation de valeur
var monArgent = 1;
var prixCafe  = 1.2;

// Condition
// Si
if ( monArgent >= prixCafe) {
    console.log("J'ai assez d'argent pour boire un café.");
}
// Sinon
else {
    console.log("Je n'ai pas assez d'argent pour boire un café.");
}
```

## Instruction else if

Cette instruction permet d'exécuter une série d'instructions lorsque plusieurs conditions sont réalisées.

La syntaxe de cette expression est la suivante :

```js
// Une première condition est testée
if ( si condition réalisée ) {
    // liste d'instructions
}
// Une deuxième condition est présente et sera testée si la première échoue
else if ( sinon si condition réalisée ) {
    // liste d'instructions
}
// Et si aucune condition ne se vérifie, la structure else fait alors son travail.
else {
    // sinon autre série d'instructions
}
```

**Exemple**

```js
// Déclaration de variable et assignation de valeur
var monArgent = 1;
var prixCafe  = 1.2;

// Condition
// Si
if ( monArgent >= (prixCafe*250) ) {
	console.log("J'ai assez pour pouvoir inviter toute l’école.");
}
// Sinon si
else if ( monArgent >= (prixCafe*30) ) {
	console.log(" J'ai assez pour pouvoir inviter toute le groupe.");
}
else if ( monArgent >= (prixCafe*2) ) {
	console.log(" J'ai assez pour pouvoir inviter mon professeur.");
}
// Sinon
else {
	console.log("Je n'ai pas assez d'argent pour boire un café. ");
}
```

## Instruction switch...case

L'instruction switch permet de faire plusieurs tests de valeurs sur le contenu d'une même variable. Ce branchement conditionnel simplifie beaucoup le test de plusieurs valeurs d'une variable. Cette opération aurait ainsi été plus compliquée (mais possible) avec des if imbriqués.

La syntaxe de cette expression est la suivante :

```js
switch (Variable) {
    case Valeur1:
        Liste d'instructions;
        break;
    case Valeur2:
        Liste d'instructions;
        break;
     default:
        Liste d'instructions;
        break;
}
```

Les parenthèses qui suivent le mot clé **switch** indiquent une expression dont la valeur est testée successivement par chacun des **case**. Lorsque l'expression testée est égale à une des valeurs suivant un **case**, la liste d'instructions qui suit celui-ci est exécutée.

Le mot clé **break** indique la sortie de la structure conditionnelle. Le mot clé **default** précède la liste d'instructions qui sera exécutée si l'expression n'est jamais égale à une des valeurs.

**Attention**, il est essentiel de terminer chaque bloc d'instructions par l'instruction **break**.<br/>
N'oubliez pas d'insérer des instructions **break** entre chaque test. Ce genre d'oubli est difficile à détecter, aucune erreur n'étant signalée.
