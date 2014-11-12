# Les fonctions

En programmation, une fonction est un sous-programme qui permet d’exécuter un ensemble d’instructions dans le corps du programme principal.

Les fonctions permettent d'exécuter dans plusieurs parties du programme une série d’instructions. Ce procédé permet une simplicité du code et donc une taille de programme minimale.

Par ailleurs, une fonction peut faire appel à elle-même. On parle alors de fonction récursive.

## Création de notre première fonction

Avant d’être utilisée, une fonction doit être déclarée afin que le navigateur l’interprète.

Une déclaration de fonction est constituée du mot-clé `function`, suivi :

1. du nom de la fonction (suit les mêmes règles que les noms de variables ) ;
2. des parenthèses **obligatoires** pouvant contenir des paramètres facultatifs séparés par des virgules ;
3. des instructions JavaScript définissant la fonction, entourés d’accolades `{ }`.<br/>Les instructions d'une fonction peuvent comprendre des appels à d'autres fonctions définies dans l'application courante.

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

Ici, pas de problème. On déclare une variable dans laquelle on stocke du texte puis on crée une fonction qui se charge de l'afficher à l'écran et enfin on l'exécute.

Les variables déclarées en dehors des fonctions sont nommées variables globales.

### Exemple 2

Modifions maintenant l’ordre des déclarations. Dans cette hypothèse, la variable sera déclarée dans la fonction.

```js
function sayHello() {
    var hello = 'Hello world !';
}
sayHello();
console.log(hello);
```

Nous pouvons nous rendre compte que cet exemple ne fonctionne pas.
Le script est arrêté car il produit une erreur (visible dans l’inspecteur web).

Voilà tout le concept de portée de variables :<br/>
Toute variable déclarée dans une fonction n'est utilisable que dans cette même fonction !
Ces variables spécifiques à une seule fonction ont un nom : les variables locales.

## Variable globale VS variable locale

Maintenant que nous savons faire la différence entre les variables globales et les variables locales, essayons de comprendre leur comportement.

Que se passe t’il si nous déclarons une variable globale et une locale avec le même nom, mais avec une autre valeur ?

```js
var hello = "Hello world !";
function sayHello() {
    var hello = "Bonjour la terre !";
    console.log("Dans la fonction : " + hello);
}
sayHello();
console.log("En dehors de la fonction : " + hello);
```
Nous obtenons le résultat suivant :

```
"Dans la fonction : Bonjour la terre !"
"En dehors de la fonction : Hello world !"
```


**Bonne pratique**<br/>
De manière générale, il est préférable d’utiliser les variables locales pour les fonctions, afin de ne pas interférer avec d’autres fonctions qui peuvent utiliser le même nom de variables.

## Les paramètres d'une fonction

Il est possible de passer des paramètres à une fonction, c'est-à-dire lui fournir une valeur ou le nom d'une variable afin que la fonction puisse effectuer des opérations sur ces paramètres.

Lorsque vous passez plusieurs paramètres à une fonction il faut les séparer par des virgules aussi bien dans la déclaration que dans l'appel. Il faudra également veiller à passer le bon nombre de paramètres lors de l'appel. Dans le cas contraire, une erreur se produira dans votre script.

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

Comme son nom l’indique, la valeur **return** est la valeur retournée par la fonction.
Les fonctions ne peuvent renvoyer qu’une valeur de retour.

```js
function Nom_De_La_Fonction(argument1, argument2) {
	return argument1 * argument2
}
```

**Attention**<br/>
L’instruction **return** met fin à la fonction, puis retourne la valeur.
Tout ce qui est renseigné en dessous est ignoré.

**Exemple**
```js
// Déclaration de la fonction
function carre(nombre) {
	return nombre * nombre;
}

// Appel de la fonction
console.log(carre(20));
```
