# Les fonctions

En programmation, une fonction est un sous-programme qui permet d’exécuter un ensemble d’instructions dans le corps du programme principal.

Les fonctions permettent d'exécuter dans plusieurs parties du programme une série d’instructions, cela permet une simplicité du code et donc une taille de programme minimale.

D'autre part, une fonction peut faire appel à elle-même, on parle alors de fonction récursive.

## Création de notre première fonction

Avant d’être utilisée, une fonction doit être déclarée afin que le navigateur l’interprète.

Une déclaration de fonction est constituée du mot-clé `function`, suivi :

1. Du nom de la fonction ( suit les mêmes règles que les noms de variables ) ;
2. D'une liste de paramètres facultatifs séparée par des virgules et entourée de parenthèses ;
3. Des instructions JavaScript définissant la fonction, entourés d’accolades `{ }`.<br/>Les instructions d'une fonction peuvent comprendre des appels à d'autres fonctions définies dans l'application courante.

La syntaxe de cette expression est la suivante.

```js
function Nom_De_La_Fonction(argument1, argument2) {
	// liste d'instructions
}
```

## Appel de notre fonction

Pour exécuter une fonction, il suffit de faire appel à elle en écrivant son nom (une fois de plus en respectant la casse) suivi d'une parenthèse ouverte (éventuellement des arguments) puis d'une parenthèse fermée.

```js
Nom_De_La_Fonction();
```

**Attention**, veillez toujours à ce qu'une fonction soit déclarée avant d'être appelée.

**Exemple**

```js
// Déclaration de la fonction
function hello () {
    console.log(‘Hello world');
}

// Appel de la fonction
hello();
```

## La portée des variables

Afin d’aborder ce concept assez simple mais pouvant induire en erreur, nous allons étudier deux exemples.

### Exemple 1
```js
var hello = "Hello world !";
function sayHello() {
    console.log(hello);
}
sayHello();
```

Ici, pas de problème. On déclare une variable dans laquelle on stocke du texte puis on créer une fonction qui se charge de l'afficher à l'écran et enfin on exécute cette dernière.

Les variables déclarées en dehors des fonctions sont nommées variables globales.

### Exemple 2

Modifions maintenait l’ordre des déclarations, la variable sera déclarée dans la fonction.

```js
function sayHello() {
    var hello = 'Hello world !';
}
sayHello();
console.log(hello);
```

Nous pouvons nous rendre compte que cet exemple ne fonctionne pas.
Le script est arrêté, car il produit une erreur (visible dans l’inspecteur web).

Voilà tout le concept de portée de variables :<br/>
Toute variable déclarée dans une fonction n'est utilisable que dans cette même fonction !
Ces variables spécifiques à une seule fonction ont un nom : les variables locales.

## Variable globale VS variable locale

Maintenant que nous savons faire la différence entre les variables globales et les variables locales, essayons de comprendre leurs comportements.

Que se passe t’il si l’ont déclare une variable globale et une locale avec le même nom, mais une autre valeur?

```js
var hello = "Hello world !";
function sayHello() {
    var hello = "Bonjour la terre !";
    console.log("Dans la fonction : " + hello);
}
sayHello();
console.log("En dehors de la fonction : " + hello);
```

**Bonne pratique**<br/>
De manière générale, il est préférable d’utiliser les variables locales pour les fonctions, afin de ne pas interférer avec d’autres fonctions qui peuvent utiliser le même nom de variables.

## Les paramètres d'une fonction

Il est possible de passer des paramètres à une fonction, c'est-à-dire lui fournir une valeur ou le nom d'une variable afin que la fonction puisse effectuer des opérations sur ces paramètres.

Lorsque vous passez plusieurs paramètres à une fonction il faut les séparer par des virgules, aussi bien dans la déclaration que dans l'appel et il faudra veiller à bien passer le bon nombre de paramètres lors de l'appel au risque sinon de créer une erreur dans votre script.

**Exemple avec un argument**

```js
// Déclaration de la fonction
function carre(nombre) {
	console.log( nombre * nombre );
}

// Appel de la fonction
carre(3);
```

**Exemple avec deux arguments**

```js
Exemple avec deux arguments
// Déclaration de la fonction
function remise(nombre, pourcentage) {
	console.log( (pourcentage / 100) * nombre );
}

// Appel de la fonction
remise(150, 20);
```

## La valeur return

Comme son nom l’indique, c’est la valeur retournée par la fonction.
Les fonctions ne peuvent renvoyer qu’une valeur de retour.

```js
function Nom_De_La_Fonction(argument1, argument2) {
	return argument1 * argument2
}
```

**Attention**<br/>
L’instruction return met fin à la fonction, puis retourne la valeur.
Tout se qui est renseigné en dessous sera ignoré.

**Exemple**
```js
// Déclaration de la fonction
function carre(nombre) {
	return nombre * nombre;
}

// Appel de la fonction
console.log(carre(20));
```
