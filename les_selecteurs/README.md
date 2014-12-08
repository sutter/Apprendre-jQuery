# Sélectionner des éléments

## De JavaScript vers jQuery

jQuery nous permet de sélectionner des éléments de façon plus simple qu'en JavaScript.

**Exemple** : Sélectionner une balise `span`

```js
// Version Javascript
document.getElementsByTagName('span');

// Version jQuery
$('span');
```

**Exemple** : Sélectionner un identifiant `#sub-footer`

```js
// Version Javascript
document.getElementById('sub-footer');

// Version jQuery
$('#sub-footer');
```

**Exemple** : Sélectionner une classe `box`

```js
// Version Javascript
document.getElementsByClassName('box');

// Version jQuery
$('.box');
```

**Exemple** : Sélectionner `#nav a:nth-child(odd)`

```js
// Version Javascript
// Ne fonctionne pas sous IE8
document.querySelectorAll('#nav a:nth-child(odd)');

// Version jQuery
// Fonctionne sous IE8
$('#nav a:nth-child(odd)');
```

Article d'Alsacréation sur `querySelector` et `querySelectorAll` : http://www.alsacreations.com/article/lire/1445-dom-queryselector-queryselectorall-selectors-api.html

## Sélectionner avec jQuery

Un des grands avantages de jQuery est d'utiliser la syntaxe des [sélecteurs CSS](http://www.w3.org/TR/css3-selectors/) et permet d'utiliser les sélecteurs CSS3 avec de vieux navigateurs.

Pour sélectionner les *noeuds du DOM* (éléments) nous utiliserons la syntaxe `$(sélecteur)`.

Bien entendu, la liste ci-dessous n'est pas exhaustive et ne reprend que les sélecteurs les plus utilisés.<br/>Vous pouvez en trouver davantage dans [l'API jQuery](http://api.jquery.com/category/selectors/).

### Combiner des sélecteurs
| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**.class, .class**](http://api.jquery.com/multiple-selector/) | `$('.box, .pod')` | Les éléments **class="box"** ou **class="pod"** |
| [**#id .class** ](http://api.jquery.com/descendant-selector/)| `$('# .box')` | Les éléments **class="box"** à l'intérieur **id=""** |
| **#id.class** | `$('#.box')` | Les éléments **class="box"** ayant pour identifiant **id=""** |
| **'.class',  '#id'** | `$('.box',  '#')` | Les éléments **class="box"** dans le contexte **id=""** |

### Les sélecteurs de base

**API :** [http://api.jquery.com/category/selectors/basic-css-selectors/](http://api.jquery.com/category/selectors/basic-css-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [*****](http://api.jquery.com/all-selector/) | `$('*')` | Tous les éléments |
| [**Balise html**](http://api.jquery.com/element-selector/) | `$('p')` | Tous les paragraphes |
| [**#id**](http://api.jquery.com/id-selector/) | `$('#header')` | Les éléments avec **id="header"** |
| [**.class**](http://api.jquery.com/class-selector/) | `$('.box')` | Les éléments avec **class="box"** |
| [**A > B**](http://api.jquery.com/child-selector/) | `$('.box > p'`) | Les élément **B** enfants directs de **A**|
| [**A + B**](http://api.jquery.com/next-adjacent-Selector/) | `$('li + li')` | L'élément **B** frère adjacent de **A** |
| [**A ~ B**](http://api.jquery.com/next-siblings-selector/) | `$('h2 ~ p')` | Les éléments **B** en dessous de **A** |

### Les sélecteurs d'enfant

**API :** [http://api.jquery.com/category/selectors/child-filter-selectors/](http://api.jquery.com/category/selectors/child-filter-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**:first-child**](http://api.jquery.com/first-child-selector/) | `$('p:first-child')` | 1<sup>er</sup> élément **p** |
| [**:last-child**](http://api.jquery.com/last-child-selector/) | `$('p:last-child')` | Dernier élément **p** |
| [**:nth-child(x)**](http://api.jquery.com/nth-child-selector/) | `$('li:nth-child(2)')` | 2<sup>ème</sup> élément **li** |
| [**:nth-child(xn + x)**](http://api.jquery.com/nth-child-selector/) | `$('li:nth-child(3n + 2)')` | 2<sup>ème</sup> élément **li** tous les 3 **li** |
| [**:only-child**](http://api.jquery.com/nth-child-selector/) | `$('.box p:only-child')` | Le fils unique **p** de **class="box"** |

### Les sélecteurs de contenu

**API :** [http://api.jquery.com/category/selectors/content-filter-selector/](http://api.jquery.com/category/selectors/content-filter-selector/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**:contains(texte)**](http://api.jquery.com/contains-selector/) | `$('p:contains("Markdown")')` | Les éléments contenant la chaîne de caractères **Markdown**.<br/>*Attention ce sélecteur est sensible à la casse* |
| [**:has(sélecteur)**](http://api.jquery.com/has-selector) | `$('.box:has(strong)')` | Les éléments **class="box"** ayant une balise **strong** |
| [**:parent**](http://api.jquery.com/parent-selector/) | `$('.box:parent')` | Les éléments **class="box"** non vides |
| [**:empty**](http://api.jquery.com/empty-selector/) | `$('.box:empty')` | Les éléments **class="box"** vides |

### Les sélecteurs d'attribut

**API :** [http://api.jquery.com/category/selectors/attribute-selectors/](http://api.jquery.com/category/selectors/attribute-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**[attr]**](http://api.jquery.com/has-attribute-selector/) | `$('[href]')` | Les éléments contenant un attribut **href** |
| [**[attr=valeur]**](http://api.jquery.com/attribute-equals-selector/) | `$('[href="index.html"]')` | Les éléments contenant un attribut **href** ayant pour valeur **index.html** |
| [**[attr!=valeur]**](http://api.jquery.com/attribute-not-equal-selector/) | `$('[href!="index.html"]')` | Les éléments contenant un attribut **href** ayant pas pour valeur **index.html** |
| [**[attr^=valeur]**](http://api.jquery.com/attribute-starts-with-selector/) | `$('[class^="box-"]')` | Les éléments ayant un classe préfixée de **box-** comme **.box-inner** |
| [**[attr$=valeur]**](http://api.jquery.com/attribute-ends-with-selector/) | `$('[class$="-active"]')` | Les éléments ayant un classe sufixée de **-active** comme **.pod-active** |
| [**[attr*=valeur]**](http://api.jquery.com/attribute-contains-selector/) | `$('[class*="box"]')` | Les éléments ayant un classe contenant **box** comme **.pod-boxed** |
| [**[attr~=valeur]**](http://api.jquery.com/attribute-contains-word-selector/) | `$('[class~="box"]')` | Les éléments ayant un classe dont la valeur est une liste séparée par des espaces dont l’un d’eux est exactement **box** comme **class="first box"** |

### Les sélecteurs de filtre

**API :** [http://api.jquery.com/category/selectors/basic-filter-selectors/](http://api.jquery.com/category/selectors/basic-filter-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**:animated**](http://api.jquery.com/animated-selector/) | `$('.box:animated')` | Les éléments **class=".box"** animés en jQuery |
| [**:eq**](http://api.jquery.com/eq-selector/) | `$('.box:eq(2)')` | Le 3<sup>ème</sup> élément **class=".box"** |
| [**:even**](http://api.jquery.com/even-selector/) | `$('tr:even')` | Les éléments **tr** pairs |
| [**:odd**](http://api.jquery.com/odd-selector/) | `$('tr:odd')` | Les éléments **tr** impairs |
| [**:first**](http://api.jquery.com/first-selector/) | `$('tr:first')` | Le premier élément **tr** trouvé |
| [**:last**](http://api.jquery.com/last-selector/) | `$('tr:last')` | Le dernier élément **tr** trouvé |
| [**:focus**](http://api.jquery.com/focus-selector/) | `$('.box:focus')` | Les éléments qui ont le **focus** |
| [**:gt**](http://api.jquery.com/gt-selector/) | `$('.box:gt(3)')` | Les éléments **class="box** à partir du 4<sup>ème</sup> |
| [**:lt**](http://api.jquery.com/gt-selector/) | `$('.box:lt(3)')` | Les éléments **class="box** jusqu'au 3<sup>ème</sup> |
| [**:header**](http://api.jquery.com/header-selector/) | `$('.title:header')` | Toutes les balises de **h1** à **h6** ayant **class="title"**|

## Les sélecteurs de visibilité

**API :** [http://api.jquery.com/category/selectors/visibility-filter-selectors/](http://api.jquery.com/category/selectors/visibility-filter-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**:hidden**](http://api.jquery.com/hidden-selector/) | `$('.box:hidden')` | Les éléments **class="box"** cachés |
| [**:visible**](http://api.jquery.com/visible-selector/) | `$('.box:visible')` | Les éléments **class=".box"** ayant une largeur ou une hauteur plus grande que **0**. |

## Les sélecteurs de formulaires

**API :** [http://api.jquery.com/category/selectors/form-selectors/](http://api.jquery.com/category/selectors/form-selectors/)

| Sélecteurs | Exemple | Éléments selectionnés |
| -- | -- | -- |
| [**:input**](http://api.jquery.com/input-selector/) | `$(:input)` | Tous les éléments de type **input** |
| [**:text**](http://api.jquery.com/text-selector/) | `$(':text')` | Les éléments **input type="text"** |
| [**:password**](http://api.jquery.com/?s=password) | `$(':password')` | Les éléments **input type="password"** |
| [**:radio**](http://api.jquery.com/radio-selector/) | `$(':radio')` | Les éléments **input type="radio"** |
| [**:checkbox**](http://api.jquery.com/?s=checkbox) | `$(':checkbox')` | Les éléments **input type="checkbox"** |
| [**:submit**](http://api.jquery.com/?s=submit) | `$(':submit')` | Les éléments **input type="submit"** |
| [**:reset**](http://api.jquery.com/reset-selector/) | `$(':reset')` | Les éléments **input type="reset"** |
| [**:button**](http://api.jquery.com/button-selector/) | `$(':button')` | Les éléments **button** |
| [**:image**](http://api.jquery.com/image-selector/) | `$(':image')` | Les éléments **input type="image"** |
| [**:file**](http://api.jquery.com/file-selector/) | `$(':file')` | Les éléments **input type="file"** |
| [**:enable**](http://api.jquery.com/enabled-selector/) | `$('input:enabled')` | Les éléments **input** actifs  |
| [**:disabled**](http://api.jquery.com/disabled-selector/) |`$('input:disabled')` | Les éléments **input** désactivés  |
| [**:selected**](http://api.jquery.com/selected-selector/) | `$('select option:selected')` | Les éléments **option** de **select** sélectionnés |
| [**:checked**](http://api.jquery.com/checked-selector/) | `$('input:checked')` | Les éléments **input** qui sont vérifiés ou sélectionnés |
