---
chapter: 6
section: a
title: Les Tableaux
description: Introduction aux tableaux en JavaScript, leur création, manipulation, particularités et pièges courants.
---

# Les Tableaux

Un **tableau** est une structure de données qui permet de stocker plusieurs valeurs dans une seule variable.  
Chaque valeur stockée est appelée un **élément**, et chaque élément est identifié par un **index**.  
Les tableaux sont très utilisés en JavaScript car ils facilitent la manipulation de collections de données.


## Création d’un tableau

Un tableau peut être créé de plusieurs manières :

```javascript
// Syntaxe littérale (recommandée)
const fruits = ["pomme", "banane", "orange"];

// Avec le constructeur Array
const numbers = new Array(1, 2, 3);

// Tableau vide
const empty = [];
```


## Accéder et modifier les éléments

L’accès aux éléments se fait par leur **index**, en commençant à `0`.

```javascript
const cars = ["Saab", "Volvo", "BMW"];
console.log(cars[0]); // "Saab"

cars[0] = "Opel"; // on change le premier élément
console.log(cars); // ["Opel", "Volvo", "BMW"]
```


## Longueur d’un tableau

La propriété `.length` retourne le nombre d’éléments :

```javascript
const fruits = ["pomme", "banane", "orange"];
console.log(fruits.length); // 3
```

!!! Attention !!! : modifier `.length` peut tronquer ou étendre le tableau en créant des “trous”.

```javascript
let a = [1, 2, 3, 4];
a.length = 2;
console.log(a); // [1, 2]

a.length = 5;
console.log(a); // [1, 2, <3 trous>]
```


## Tableaux multidimensionnels

Un tableau peut contenir d’autres tableaux, ce qui permet de créer des **tableaux multidimensionnels** (ou “matrices”).

```javascript
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

console.log(matrix[0][1]); // 2
console.log(matrix[2][0]); // 7
```


## Les tableaux sont des objets

En JavaScript, les tableaux sont en réalité un **type spécial d’objet**.
C’est pourquoi :

```javascript
console.log(typeof []);           // "object"
console.log(Array.isArray([]));   // true
```

Il faut utiliser `Array.isArray()` pour vérifier si une variable est bien un tableau.

De plus, un tableau peut recevoir des **propriétés nommées** comme un objet, mais ce n’est pas conseillé :

```javascript
let arr = [1, 2, 3];
arr["foo"] = "bar";
console.log(arr.foo);     // "bar"
console.log(arr.length);  // 3 (inchangé)
```

Les indices valides sont toujours des **entiers non négatifs**. Les clés non numériques font de votre tableau un objet hybride, ce qui complique le code.

---

## À retenir

* Les tableaux stockent plusieurs valeurs dans une seule variable.
* L’indexation commence à `0`.
* `.length` indique le nombre d’éléments, mais sa modification peut tronquer ou étendre le tableau.
* Les tableaux peuvent être **multidimensionnels**.
* Ce sont des **objets spéciaux** : utilisez `Array.isArray()` pour les identifier correctement.
* Évitez d’utiliser des clés non numériques dans un tableau.

---

⬅️ [Chapitre précédent : Conditions](../05_conditional/g_Exercices.md)

➡️ [Chapitre suivant : Méthodes des tableaux](./x_methodes.md)
