# Les variables

Une variable est un objet repéré par son nom, pouvant contenir tout type de données, qui pourront être modifiées lors de l'exécution du programme.

En JavaSript les noms de variables peuvent être aussi long que l’ont le souhaite, mais doivent répondre à certains critères :

1. un nom de variable doit commencer par une lettre (majuscule ou minuscule) ou un `_` underscore.
2. un nom de variable peut comporter des lettres, des chiffres et les caractères `_`et `&`.
3. **les espaces ne sont pas autorisés**
4. Les noms de variables ne peuvent pas être les noms suivants, qui sont des noms réservés :<br/><small>*abstract, boolean, break, byte, case, catch, char, class, const, continue, debugger, default, delete, do, double, else, export, extends, false, final, finally, float, for, function, goto, if, implements, import, in, infinity, instanceof, int, interface, label, long, native, new, null, package, private, protected, public, return, short, static, super, switch, synchronized, this, throw, throws, transient, true, try, typeof, var, void, volatile, while, with.*</small>

## Création de notre première variable

Nous déclarons notre variable.
```js
var maVariable;
```

Le mot clé **var** indique que vous déclarez une variable, `;` indique que l'instruction est terminée.
Une fois déclarée, **var** n'est plus nécessaire, vous pouvez stoker ce que vous souhaitez.

```js
var maVariable;
maVariable = "J'aime JavaScript";
```

Nous pouvons modifier la valeur de la variable.

```js
var maVariable;
maVariable = "J'aime JavaScript";
maVariable = "Je n'ai pas peur de JavaScript";
// maVariable vaut "Je n'ai pas peur de JavaScript
```

Nous pouvons déclarer notre variable et lui attribuer une valeur sur la même ligne.

```js
var maVariable_2 = 7;
```

Nous pouvons déclarer plusieurs variables sur une ligne, mais attribuer une valeur seulement à *maVariable_*2.

Puisque l'ont délare le même type d'élément, le mot clé `var` peut éviter d'être répété en séparant les déclarations par des virgules.

```js
var maVariable_1,
    maVariable_2 = 7,
    maVariable_3;
```

Vous pouvez afficher votre 1ère variable dans la console de votre navigateur.

```js
var maVariable = "J'aime JavaScript";
console.log(maVariable);
```
