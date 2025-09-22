---
chapter: 8
section: b
title: Fonctions d’ordre supérieur
description: Les fonctions d’ordre supérieur manipulent d’autres fonctions. Elles peuvent les recevoir en argument ou les renvoyer comme résultat, ce qui permet d’écrire du code puissant, expressif et réutilisable.
---

# Fonctions d’ordre supérieur

En JavaScript, les fonctions ne sont pas seulement des blocs de code que l’on exécute : ce sont aussi des valeurs à part entière. Cela signifie qu’elles peuvent être stockées dans des variables, transmises en argument ou même renvoyées en résultat. On appelle **fonctions d’ordre supérieur** celles qui manipulent d’autres fonctions.  

Concrètement, une fonction d’ordre supérieur peut recevoir une fonction en paramètre, l’appliquer à une série de données, ou bien produire une nouvelle fonction adaptée à un besoin particulier. Ces mécanismes, que l’on retrouve dans d’autres langages comme Python ou Lisp, ouvrent la porte à une programmation plus expressive et modulaire.



## Exemple avec map

Commençons avec un exemple classique. Définissons deux fonctions simples :

```javascript
let add_2 = function (x) {
  return x + 2;
};

let double = function (x) {
  return 2 * x;
};
```

Créons maintenant une fonction d’ordre supérieur appelée `map`. Celle-ci prend deux arguments : une fonction `func` et un tableau `list`. Elle applique `func` à chaque élément du tableau et renvoie le tableau transformé :

```javascript
let map = function (func, list) {
  let output = [];
  for (let idx in list) {
    output.push(func(list[idx]));
  }
  return output;
};

map(add_2, [5, 6, 7]);   // => [7, 8, 9]
map(double, [5, 6, 7]);  // => [10, 12, 14]
```

Ici, `map` agit comme un intermédiaire : elle ne connaît pas à l’avance la transformation à effectuer, mais elle délègue cette responsabilité à la fonction reçue en argument.



## Générer des fonctions spécialisées

Puisque nous appelons souvent `map(add_2, ...)` ou `map(double, ...)`, il peut être utile de créer des fonctions spécialisées. On peut le faire en composant des fonctions :

```javascript
let process_add_2 = function (list) {
  return map(add_2, list);
};

let process_double = function (list) {
  return map(double, list);
};

process_add_2([5, 6, 7]);   // => [7, 8, 9]
process_double([5, 6, 7]);  // => [10, 12, 14]
```

Pour éviter de dupliquer ce schéma, écrivons une fonction d’ordre supérieur qui fabrique automatiquement ce genre de processeur :

```javascript
let buildProcessor = function (func) {
  return function (list) {
    return map(func, list);
  };
};

let process_add_2 = buildProcessor(add_2);
let process_double = buildProcessor(double);

process_add_2([5, 6, 7]);   // => [7, 8, 9]
process_double([5, 6, 7]);  // => [10, 12, 14]
```

Ainsi, avec une seule fonction générique (`buildProcessor`), nous générons des fonctions spécialisées adaptées à chaque transformation.



## Créer des fonctions sur mesure

Les fonctions d’ordre supérieur permettent aussi de construire des générateurs de fonctions. Prenons l’exemple d’un **multiplicateur** :

```javascript
let buildMultiplier = function (x) {
  return function (y) {
    return x * y;
  };
};

let double = buildMultiplier(2);
let triple = buildMultiplier(3);

double(3); // => 6
triple(3); // => 9
```

Ici, `buildMultiplier` fabrique de nouvelles fonctions capables de multiplier n’importe quel nombre par une valeur donnée. L’intérêt est clair : on crée à la volée des outils adaptés à un usage spécifique.

---

## À retenir

Les **fonctions d’ordre supérieur** illustrent la puissance de JavaScript en tant que langage fonctionnel.
Elles rendent possible la composition, la création de fonctions spécialisées, et une écriture plus concise et expressive. Grâce à elles, le code devient à la fois plus flexible et plus réutilisable.

---

⬅️ [Chapitre précédent : Les Fonctions](./a_Fonctions.md)

➡️ [Chapitre suivant : Les Paramètres](./c_Parametres.md)
