---
chapter: 2
section: d
title: Les Types
description: Les types peuvent être vus comme les sortes de données qui possèdent une représentation dans le langage et qui peuvent être manipulés.
---

# Les Types

Les ordinateurs sont sophistiqués et peuvent manipuler des variables plus complexes qu'un simple nombre. C'est ainsi que les **types** entrent en jeu.  
Les variables se décomposent en différentes catégories. Les types supportés sont propres à chaque langage de programmation.

En JavaScript, les types les plus courants sont :

- **Nombres** : entiers (`1`, `-5`, `100`) ou décimaux (`3.14`, `-2.5`, `0.01`). JavaScript ne distingue pas les deux, il les considère toujours comme des `number`.  
- **Chaînes de caractères** (*strings*) : séquences de caractères entourées de guillemets simples (`'hello'`) ou doubles (`"world"`).  
- **Booléens** : valeurs `true` ou `false`.  
- **Null** : représente une absence de valeur.  
- **Undefined** : représente une variable déclarée mais non initialisée.  
- **Objets** : ensembles de propriétés sous forme de paires nom/valeur, déclarés entre accolades `{}`.  
- **Tableaux** : objets particuliers faits pour stocker des listes de valeurs, créés avec des crochets `[]`.  
- **Fonctions** : blocs de code réutilisables qui prennent des arguments et renvoient une valeur, créés avec le mot clé `function`.

JavaScript est un langage **faiblement typé**, c’est-à-dire que vous n’avez pas besoin d’indiquer explicitement le type de vos variables. Le moteur JavaScript déduit le type automatiquement à partir de la valeur assignée.

## Exercice 1

Déclarez trois variables et initialisez-les avec les valeurs suivantes :  

- `age` doit être un nombre,  
- `name` doit être une chaîne de caractères,  
- `isMarried` doit être un booléen.  

### Exemple de solution

```javascript
let age = 30;
let name = "Cecilia";
let isMarried = true;
```

## L’opérateur typeof

L’opérateur `typeof` est utilisé pour déterminer le type d’une variable :

```javascript
typeof "John";              // "string"
typeof 3.14;                // "number"
typeof NaN;                 // "number"
typeof false;               // "boolean"
typeof [1, 2, 3, 4];        // "object"
typeof { name: "John" };    // "object"
typeof new Date();          // "object"
typeof function () {};      // "function"
typeof myCar;               // "undefined"
typeof null;                // "object"
```

---

## Types de données

En JavaScript, on distingue deux grandes catégories :

1. Les types qui peuvent contenir des valeurs :
   
   * `string`
   
   * `number`
   
   * `boolean`
   
   * `object`
   
   * `function`
   
   > Note : `Object`, `Date`, `Array`, `String`, `Number` et `Boolean` sont des objets natifs disponibles en JavaScript.

2. Les types qui ne peuvent pas contenir de valeurs :
   
   * `null`
   * `undefined`

Une **valeur primitive** est une donnée simple sans propriété ni méthode, qui n’est pas un objet. Les primitives sont immuables (elles ne peuvent pas être modifiées).
Il existe 7 types primitifs en JavaScript :
`string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`.

---

## Exercice 2

Déclarez une variable `person` et initialisez-la comme un objet avec les propriétés suivantes :

* `age` (un nombre)
* `name` (une chaîne)
* `isMarried` (un booléen)

### Exemple de solution

```javascript
let person = {
  name: "Mary",
  age: 25,
  isMarried: false
};
```

---

## À retenir

- Les principaux **types de données** en JavaScript sont : `number`, `string`, `boolean`, `null`, `undefined`, `object`, `function`.  
- JavaScript est **faiblement typé** : on n’a pas besoin d’indiquer le type d’une variable, il est déduit automatiquement.  
- L’opérateur `typeof` permet de déterminer le type d’une valeur.  
- Les **données primitives** sont simples et immuables (ex. `string`, `number`), contrairement aux objets.  

---

⬅️ [Chapitre précédent : Égalité](./c_Egalite.md)

➡️ [Chapitre suivant : Exercices](./e_Exercices.md)
