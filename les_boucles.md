# Les boucles

Les boucles sont des structures qui permettent d'exécuter plusieurs fois la même série d'instructions jusqu'à ce qu'une condition ne soit plus réalisée.

La façon la plus commune de faire une boucle est de créer un compteur (une variable qui s'incrémente, c'est-à-dire qui augmente de 1 à chaque tour de boucle) et de faire arrêter la boucle lorsque le compteur dépasse une certaine valeur.

## L'instruction for

L'instruction `for` permet d'exécuter plusieurs fois la même série d'instructions: c'est une boucle !

Dans sa syntaxe, il suffit de préciser le nom de la variable qui sert de compteur et éventuellement sa valeur de départ, la condition sur la variable pour laquelle la boucle s'arrête (basiquement une condition qui teste si la valeur du compteur dépasse une limite) et enfin une instruction qui *incrémente* ou *décrémente* le compteur.

La syntaxe de cette expression est la suivante :

```js
for (compteur; condition; modification du compteur) {
	// liste d'instructions
}
```

**Exemple**

```js
var i;
for (i=1; i<6; i++) {
    console.log(i);
}
```

Cette boucle affiche 5 fois la valeur de i, c'est-à-dire 1,2,3,4,5

Elle commence à `i=1`, vérifie que i est bien inférieur à 6, etc... jusqu'à atteindre la valeur `i=6`, pour laquelle la condition ne sera plus réalisée, la boucle s'interrompra et le programme continuera son cours.


1. Il faudra toujours vérifier que la boucle a bien une condition de sortie
2. Une instruction `Alert(i)`; dans votre boucle est un bon moyen pour vérifier la valeur du compteur pas à pas!
3. Il faut bien compter le nombre de fois que l'on veut faire exécuter la boucle:
    * `for(i=0;i<10;i++)` exécute 10 fois la boucle (i de 0 à 9)
    * `for(i=0;i<=10;i++)` exécute 11 fois la boucle (i de 0 à 10)
	* `for(i=1;i<10;i++)` exécute 9 fois la boucle (i de 1 à 9)
	* `for(i=1;i<=10;i++)` exécute 10 fois la boucle (i de 1 à 10)

## L'instruction while

L'instruction `while` représente un autre moyen d'exécuter plusieurs fois la même série d'instructions.

La syntaxe de cette expression est la suivante.

```js
while (condition réalisée) {
    // liste d'instructions
}
```

Cette instruction exécute la liste d'instructions **tant que** la condition est réalisée.

**Attention** aux boucles infinies (boucle dont la condition est toujours vraie) provoque un plantage du navigateur!

**Exemple**

```js
var x = 0;
while(x < 10) {
    console.log("I'm looping!");
    x++;
}
```
