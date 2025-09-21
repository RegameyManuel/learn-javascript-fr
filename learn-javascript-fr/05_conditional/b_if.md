---
chapter: 5
section: b
title: L’instruction if
description: Découvrir comment utiliser l’instruction if en JavaScript pour exécuter du code selon qu’une condition est vraie ou fausse.
---

# L’instruction if

L’instruction `if` permet d’exécuter une portion de code uniquement si une condition est remplie.  
C’est la manière la plus simple d’introduire de la logique conditionnelle dans un programme.


## Exemple simple

```javascript
let x = 5;

if (x > 2) {
  console.log("x est supérieur à 2");
}
```

Ici, le test `x > 2` est vrai, donc l’instruction `console.log("x est supérieur à 2")` est exécutée.
Si la condition avait été fausse, le code à l’intérieur des accolades n’aurait pas été exécuté.


## Plusieurs conditions indépendantes

On peut placer plusieurs instructions `if` à la suite pour tester différentes conditions :

```javascript
let country = "France";
let weather;
let food;
let currency;

if (country === "Angleterre") {
  weather = "horrible";
  food = "passable";
  currency = "livre sterling";
}

if (country === "France") {
  weather = "agréable";
  food = "formidable, mais peu adaptée aux végétariens";
  currency = "marrante, petite et colorée";
}

if (country === "Allemagne") {
  weather = "correct";
  food = "vraiment pas bon";
  currency = "marrante, petite et colorée";
}

let message =
  "Il s'agit de la " +
  country +
  ", le temps est " +
  weather +
  ", la nourriture est " +
  food +
  " et la " +
  "monnaie est " +
  currency;

console.log(message);
// 'Il s'agit de la France, le temps est agréable, la nourriture est formidable, mais peu adaptée aux végétariens et la monnaie est marrante, petite et colorée'
```

Dans ce cas, chaque condition est évaluée séparément.
Il est possible qu’aucun bloc ne soit exécuté, ou bien qu’un seul s’exécute, ou même que plusieurs blocs s’exécutent si plusieurs conditions sont vraies.


## Exercice

Déclarez une variable `age` et attribuez-lui la valeur `20`.
Utilisez une instruction `if` pour afficher le message `"Majeur"` uniquement si l’âge est supérieur ou égal à 18.

### Solution attendue

```javascript
let age = 20;

if (age >= 18) {
  console.log("Majeur");
}
```

---

## À retenir

* L’instruction `if` teste une condition et exécute un bloc de code si cette condition est `true`.
* Si la condition est `false`, le bloc est ignoré.
* On peut écrire plusieurs `if` indépendants pour tester des cas différents.

---

⬅️ [Chapitre précédent : Logique conditionnelle](./a_Logique.md)

➡️ [Chapitre suivant : Else](./c_else.md)

