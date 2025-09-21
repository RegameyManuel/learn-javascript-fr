---
chapter: 2
section: b
title: Les Variables
description: Les variables sont utilisées stockées et mémoriser des données. Il est possible de stocker différents types de données dans les variables comme des nombres, des chaînes de caractères, des booléens, des objets, des tableaux, des fonctions et autres.
---

# Les Variables

Afin de bien comprendre la programmation, la première étape consiste à se rappeler l'algèbre.  
En mathématiques, on écrit par exemple :

```javascript

3 + 5 = 8

```

On peut introduire une inconnue, comme `x` :

```javascript

3 + x = 8

```

En déplaçant les termes, on trouve la valeur de `x` :

```javascript

x = 8 - 3
-> x = 5

```

Avec plusieurs inconnues, les combinaisons sont multiples :

```javascript

x + y = 8

```

On peut obtenir :

```javascript

x = 4
y = 4

```

ou encore :

```javascript

x = 3
y = 5

```

En programmation, les variables fonctionnent de manière similaire : elles sont comme de petites boîtes dont le contenu peut changer. Elles contiennent des valeurs ou le résultat de calculs. Chaque variable possède un **nom** et une **valeur**, séparés par un signe égal `=`.  
Attention : certains mots sont **réservés** et ne peuvent pas être utilisés comme noms de variables.


## Déclaration de variables en JavaScript

Exemple simple : définir deux variables, calculer leur somme et stocker le résultat dans une troisième variable :

```javascript
let x = 5;
let y = 6;
let result = x + y;
```


## Règles de nommage

Il existe des règles précises à respecter :

* Le nom d'une variable doit commencer par une lettre, un underscore (`_`) ou un signe dollar (`$`).
* Après le premier caractère, on peut utiliser des lettres, chiffres, underscores ou signes dollar.
* JavaScript est **sensible à la casse** : `maVariable`, `MaVariable` et `MAVARIABLE` sont trois variables distinctes.
* Il est recommandé d’utiliser des noms **clairs et descriptifs** qui reflètent le rôle de la variable.


## Exercice

Définissez une variable `x` égale à 20.

### Code de départ

```javascript
let x =
```

### Solution attendue

```javascript
let x = 20;
```


## ES6 et les nouvelles déclarations

Depuis **ECMAScript 2015 (ES6)**, JavaScript offre trois mots-clés pour déclarer des variables : `var`, `let` et `const`.

```javascript
var x = 5;
const y = "Test";
let z = true;
```

La différence principale se situe au niveau de la portée :

* `var` définit une variable accessible dans toute la fonction ou globale si déclarée hors fonction.
* `let` limite l’utilisation de la variable au bloc (`{ ... }`) dans lequel elle est déclarée.
* `const` crée une variable dont la valeur ne peut plus être modifiée après sa déclaration.


## Exemple var vs let

```javascript
function varTest() {
  var x = 1;
  if (true) {
    var x = 2; // on agit sur la même variable
    console.log(x); // 2
  }
  console.log(x); // 2
}

function letTest() {
  let x = 1;
  if (true) {
    let x = 2; // variable différente dans le bloc
    console.log(x); // 2
  }
  console.log(x); // 1
}
```


## Exemple const

```javascript
const x = "hi!";
x = "bye"; 
// Ceci provoquera une erreur : une variable const ne peut pas être réassignée
```

---

## À retenir

- Une **variable** est une “boîte” qui contient une valeur.  
- En JavaScript, on peut déclarer une variable avec `var`, `let` ou `const`.  
- `let` est privilégié pour les valeurs modifiables, `const` pour les constantes, `var` est ancien et à éviter.  
- JavaScript est **sensible à la casse** : `maVariable` ≠ `MaVariable`.  

---


⬅️ [Chapitre précédent : Les Commentaires](./a_Commentaires.md)

➡️ [Chapitre suivant : Égalité](./c_Egalite.md)