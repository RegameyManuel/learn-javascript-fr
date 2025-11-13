---
chapter: 3
section: a
title: Les nombres en JavaScript
description: Comprendre comment JavaScript gère les nombres et découvrir leurs particularités.
---

# Les nombres en JavaScript

En JavaScript, il n’existe qu’un seul type de nombre : les **flottants 64 bits**.  
Cela signifie qu’il n’y a **pas de différence entre un entier et un nombre décimal** : tout est stocké de la même manière en mémoire.  

Autrement dit, que vous écriviez `42` ou `3.14`, il s’agit toujours du même type : `number`.  
Ce choix de conception simplifie le langage, mais entraîne aussi des particularités qu’il faut bien comprendre.

```javascript
let entier = 42;
let decimal = 3.14;

console.log(entier);   // 42
console.log(decimal);  // 3.14
```

## Équivalence et précision

Contrairement à d’autres langages qui distinguent plusieurs catégories (`int`, `float`, `double`), JavaScript ne fait **aucune différence** entre `1` et `1.0`.

```javascript
console.log(1 === 1.0); // true
```

C’est une simplification bienvenue, mais elle a un coût : comme tout est stocké en **flottant 64 bits**, la précision est limitée.
En pratique, JavaScript ne peut garantir que **15 à 17 chiffres significatifs**.

Cela entraîne parfois des résultats inattendus, surtout avec les nombres décimaux :

```javascript
console.log(0.1 + 0.2); // 0.30000000000000004
```

Ici, le résultat n’est pas exactement `0.3` car le binaire, qui est la base du fonctionnement des ordinateurs, ne peut pas représenter certains nombres décimaux de façon parfaite.
De la même manière qu’en décimal on ne peut pas écrire 1/3 exactement (0.3333...), en binaire certains nombres n’ont pas de représentation finie.

## Nombres spéciaux

JavaScript définit aussi des valeurs particulières qui appartiennent au type `number` :

```javascript
console.log(1 / 0);     // Infinity
console.log(-1 / 0);    // -Infinity
console.log(0 / 0);     // NaN (Not a Number)
```

`Infinity` et `-Infinity` représentent respectivement l’infini positif et négatif.

`NaN` signifie *Not a Number*. C’est le résultat d’une opération qui n’a pas de sens mathématique, comme `0 / 0` ou `"abc" * 5`.

 !!! Attention !!!  : `NaN` est contagieux. Toute opération impliquant `NaN` donnera `NaN`.

## Bases différentes

JavaScript permet de représenter les nombres dans plusieurs systèmes de numération.

* **Décimal** : la base habituelle (ex. `42`).
* **Hexadécimal** : préfixé par `0x` (ex. `0xFF` → 255).
* **Binaire** : préfixé par `0b` (ex. `0b1010` → 10).
* **Octal** : préfixé par `0o` (ex. `0o12` → 10).

```javascript
let hex = 0xFF;   // 255 en hexadécimal
let bin = 0b1010; // 10 en binaire
let oct = 0o12;   // 10 en octal

console.log(hex, bin, oct);
```

Ces notations sont pratiques, surtout dans le domaine des systèmes, des algorithmes bas-niveau ou pour manipuler des couleurs (`#FF0000` en hexadécimal = rouge).

## Limites numériques

L’objet `Number` met à disposition plusieurs constantes utiles pour connaître les limites de ce qui peut être représenté en JavaScript :

```javascript
console.log(Number.MAX_VALUE);        // plus grand nombre représentable
console.log(Number.MIN_VALUE);        // plus petit nombre positif (≈ 5e-324)
console.log(Number.MAX_SAFE_INTEGER); // plus grand entier sûr (≈ 9e15)
console.log(Number.MIN_SAFE_INTEGER); // plus petit entier sûr (≈ -9e15)
```

Les **entiers sûrs** sont ceux qui peuvent être représentés exactement sans perte de précision.

Au-delà de ces bornes, JavaScript risque d’arrondir ou d’approximer.

## Comment bien travailler avec les nombres ?

1. **Accepter la limite de précision** : JavaScript n’est pas fait pour des calculs scientifiques extrêmement précis. Pour cela, on utilise des bibliothèques spécialisées (BigInt, decimal.js…).
2. **Se méfier de `NaN`** : toujours vérifier vos calculs si un résultat inattendu apparaît.
3. **Utiliser les bonnes conversions** : `parseInt`, `parseFloat` et `Number()` permettent de transformer des chaînes en nombres.

## Exercice

1. Crée deux variables `a` et `b` contenant respectivement `0.1` et `0.2`. Additionne-les et affiche le résultat. Explique pourquoi le résultat n’est pas exactement `0.3`.
2. Déclare un nombre en binaire (`0b1011`) et affiche sa valeur décimale.
3. Trouve le plus grand entier sûr avec `Number.MAX_SAFE_INTEGER`. Ajoute `1` puis `2` et observe le résultat.

---

## À retenir

* En JavaScript, il n’existe qu’un seul type de nombre : les **flottants 64 bits**.
* Tous les nombres (entiers ou décimaux) sont du type `number`.
* La précision est limitée à **15-17 chiffres significatifs**, d’où des résultats étranges comme `0.1 + 0.2`.
* Des valeurs spéciales existent : `NaN`, `Infinity`, `-Infinity`.
* Les nombres peuvent être exprimés en **décimal**, **hexadécimal**, **binaire** et **octal**.
* L’objet `Number` fournit des constantes comme `MAX_VALUE` et `MAX_SAFE_INTEGER` pour connaître les limites.

---

⬅️ [Chapitre précédent : Bases](../02_basics/e_Exercices.md)

➡️ [Chapitre suivant : Math](./b_Math.md)
