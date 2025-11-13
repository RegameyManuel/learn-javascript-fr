---
chapter: 14
section: a
title: Expressions régulières
description: Une expression régulière (regex) est un outil puissant pour rechercher, comparer et manipuler du texte en fonction de modèles précis.
---

# Expressions régulières

Les expressions régulières, souvent abrégées en *regex*, constituent un langage spécialisé destiné à la recherche et à la manipulation de chaînes de caractères. Elles permettent de définir des modèles capables de détecter des motifs précis dans un texte, d’extraire des parties correspondantes ou encore de remplacer certains éléments.

En JavaScript, une expression régulière peut être créée de deux manières : soit grâce au constructeur `RegExp`, soit en utilisant la notation littérale entourée de barres obliques.

```javascript
// Avec le constructeur
let re1 = new RegExp("xyz");

// Avec la notation littérale
let re2 = /xyz/;
```

Dans les deux cas, on obtient un objet `RegExp` qui dispose des mêmes propriétés et méthodes. L’usage du constructeur est utile lorsqu’on veut construire une regex dynamiquement à partir de variables, tandis que la notation littérale est plus concise dans la plupart des cas.

## Les modificateurs

Une regex peut être enrichie de modificateurs, appelés aussi drapeaux, qui changent la manière dont elle s’applique :

* `g` : recherche globale, pour trouver toutes les occurrences au lieu de s’arrêter à la première,
* `i` : recherche insensible à la casse,
* `m` : recherche multilignes.

Par exemple :

```javascript
let pattern = /hello/gi;
```

Ici, la recherche de « hello » sera effectuée sans tenir compte de la casse et sur l’ensemble du texte.

## Les ensembles de caractères

Les crochets `[ ]` permettent de cibler une plage de caractères ou un groupe défini :

* `[abc]` : trouve un caractère parmi `a`, `b` ou `c`,
* `[^abc]` : trouve un caractère qui n’est pas `a`, `b` ou `c`,
* `[0-9]` : trouve un chiffre,
* `[^0-9]` : trouve un caractère qui n’est pas un chiffre,
* `(x|y)` : trouve l’une des alternatives proposées.

## Les métacaractères

Les regex reposent sur des caractères spéciaux, appelés **métacaractères**, qui enrichissent considérablement leur expressivité.

| Métacaractère | Description                                                        |
| ------------- | ------------------------------------------------------------------ |
| `.`           | Correspond à n’importe quel caractère sauf la nouvelle ligne       |
| `\w`          | Correspond à un caractère alphanumérique `[a-zA-Z0-9_]`            |
| `\W`          | Correspond à tout caractère non alphanumérique                     |
| `\d`          | Correspond à un chiffre `[0-9]`                                    |
| `\D`          | Correspond à un caractère qui n’est pas un chiffre                 |
| `\s`          | Correspond à un espace (espace, tabulation, etc.)                  |
| `\S`          | Correspond à un caractère qui n’est pas un espace                  |
| `\b`          | Correspond au début ou à la fin d’un mot                           |
| `\B`          | Correspond à tout sauf le début ou la fin d’un mot                 |
| `\0`          | Correspond au caractère NULL                                       |
| `\n`          | Correspond à un retour à la ligne                                  |
| `\f`          | Correspond à un saut de page                                       |
| `\r`          | Correspond à un retour chariot                                     |
| `\t`          | Correspond à une tabulation                                        |
| `\v`          | Correspond à une tabulation verticale                              |
| `\xxx`        | Correspond à un caractère défini par un code octal                 |
| `\xdd`        | Correspond à un caractère défini par un code hexadécimal           |
| `\udddd`      | Correspond à un caractère Unicode défini par un nombre hexadécimal |

## Propriétés et méthodes

Les objets `RegExp` possèdent différentes propriétés et méthodes pour travailler avec les modèles :

| Nom           | Description                                                              |
| ------------- | ------------------------------------------------------------------------ |
| `constructor` | Renvoie la fonction qui a créé le prototype de l’objet `RegExp`          |
| `global`      | Indique si le modificateur `g` est activé                                |
| `ignoreCase`  | Indique si le modificateur `i` est activé                                |
| `lastIndex`   | Position à laquelle commencera la recherche suivante                     |
| `multiline`   | Indique si le modificateur `m` est activé                                |
| `source`      | Retourne le texte du modèle de l’expression régulière                    |
| `exec()`      | Renvoie la première correspondance trouvée ou `null`                     |
| `test()`      | Renvoie `true` ou `false` selon que le modèle correspond au texte ou non |
| `toString()`  | Renvoie la représentation en chaîne de l’expression régulière            |

 La méthode `compile()` existe encore mais est obsolète et ne doit plus être utilisée.

## Exemples d’utilisation

Voici quelques exemples concrets d’utilisation des regex en JavaScript :

```javascript
let text = "Les meilleures choses dans la vie sont gratuites";

// Chercher la première occurrence de la lettre "e"
let result = /e/.exec(text);
console.log(result[0]); // "e"

let helloWorldText = "Hello world!";

// Tester la présence du mot "Hello"
let pattern1 = /Hello/g;
console.log(pattern1.test(helloWorldText)); // true

// Obtenir la chaîne représentant le motif
let pattern1String = pattern1.toString();
console.log(pattern1String); // "/Hello/g"
```

Les expressions régulières permettent ainsi d’exprimer des recherches complexes en quelques caractères, ce qui en fait un outil précieux pour l’analyse et le traitement de texte.

---

## À retenir

Les expressions régulières (regex) servent à rechercher et manipuler des chaînes de caractères selon des motifs précis.
Elles peuvent être définies avec le constructeur `RegExp` ou par une notation littérale, enrichies de modificateurs comme `g`, `i` et `m`.
Elles reposent sur des ensembles de caractères, des métacaractères et des méthodes dédiées (`test`, `exec`, etc.).
Bien qu’elles puissent paraître difficiles à lire au premier abord, elles offrent une puissance et une flexibilité inégalées pour travailler avec du texte.

---

⬅️ [Chapitre précédent : Modules](../13_modules/b_Exercices.md)

➡️ [Chapitre suivant : Exercices](./b_Exercices.md)
