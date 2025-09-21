---
chapter: 4
section: e
title: Concaténation de chaînes
description: Découvrir comment combiner plusieurs chaînes de caractères en JavaScript en utilisant l’opérateur + ou les littéraux de gabarits.
---

# Concaténation de chaînes

La **concaténation** est l’action de mettre bout à bout plusieurs chaînes de caractères afin d’en former une seule.  
En JavaScript, il existe deux manières principales de concaténer des chaînes : l’opérateur `+` et les littéraux de gabarits (introduits avec ES6).


## Avec l’opérateur +

La méthode la plus simple consiste à utiliser l’opérateur `+` :

```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName;

console.log(fullName); // John Doe
```

Dans cet exemple, un espace a été ajouté entre `firstName` et `lastName` pour obtenir un résultat plus lisible.


## Avec les littéraux de gabarits

Depuis ES6, les littéraux de gabarits (délimités par des backticks `` ` ``) permettent une concaténation plus lisible :

```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = `${firstName} ${lastName}`;

console.log(fullName); // John Doe
```

Cette méthode est aujourd’hui largement préférée, car elle est plus claire et permet d’intégrer directement des variables ou expressions.


## Exercice

1. Déclarez deux variables : `city = "Paris"` et `country = "France"`.
2. Créez une nouvelle variable `location` qui combine les deux valeurs.
3. Le résultat attendu est : `"Paris, France"`.


### Solution attendue

```javascript
let city = "Paris";
let country = "France";

let location = city + ", " + country;
console.log(location); // Paris, France
```

Ou, avec un littéral de gabarit :

```javascript
let location = `${city}, ${country}`;
console.log(location); // Paris, France
```

---

## À retenir

* L’opérateur `+` permet de concaténer des chaînes, mais peut vite devenir difficile à lire.
* Les littéraux de gabarits sont plus modernes et plus pratiques pour intégrer des variables ou des expressions.

---

⬅️ [Chapitre précédent : Longueur des chaînes](./d_Longueur.md)
➡️ [Chapitre suivant : Exercices](./f_Exercices.md)

