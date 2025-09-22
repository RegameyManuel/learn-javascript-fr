---
chapter: 8
section: d
title: Les Portées
description: La portée détermine l’endroit où une variable est accessible dans un programme. En JavaScript, on distingue la portée globale, locale et de bloc. Les fermetures (closures) prolongent cette idée en permettant à une fonction de se souvenir de son environnement.
---

# Les Portées

Lorsqu’on écrit du code, toutes les variables n’ont pas la même « visibilité ». Certaines peuvent être utilisées partout, d’autres seulement dans une fonction ou un bloc donné. Cette notion est appelée **portée** (ou *scope* en anglais). Elle définit l’endroit où une variable est accessible, et elle joue un rôle essentiel dans l’organisation et la sécurité du code.



## Portée globale

Une variable déclarée en dehors de toute fonction ou bloc appartient à la **portée globale**.  
Elle est accessible depuis n’importe quelle partie du programme :

```javascript
let message = "Bonjour";

function saluer() {
  console.log(message); // accessible
}

saluer();
console.log(message); // toujours accessible
```

Attention toutefois : les variables globales peuvent provoquer des conflits si elles sont trop nombreuses. C’est pourquoi il est recommandé de les limiter au strict nécessaire.



## Portée locale

Lorsqu’une variable est déclarée à l’intérieur d’une fonction, elle n’est visible qu’à l’intérieur de cette fonction. On parle alors de **portée locale** :

```javascript
function saluer() {
  let texte = "Salut !";
  console.log(texte); // accessible ici
}

saluer();
console.log(texte); // Erreur : texte n’existe pas en dehors
```

Chaque fonction définit ainsi son propre environnement isolé.



## Portée de bloc

Avec les mots-clés modernes `let` et `const`, JavaScript introduit la **portée de bloc**.
Une variable définie à l’intérieur d’accolades `{ ... }` n’est accessible qu’à l’intérieur de ce bloc, qu’il s’agisse d’une condition ou d’une boucle.

```javascript
if (true) {
  let a = 42;
  console.log(a); // accessible
}

console.log(a); // Erreur : a n’est pas défini
```

En revanche, avec `var`, la portée est uniquement fonctionnelle et non pas limitée au bloc. Cela peut entraîner des comportements surprenants :

```javascript
if (true) {
  var b = 99;
}
console.log(b); // 99, car var ignore la portée de bloc
```

C’est l’une des raisons pour lesquelles `let` et `const` sont aujourd’hui préférés.



## Les fermetures (closures)

Un concept plus avancé lié à la portée est celui de la **fermeture**.
Une fermeture est une fonction qui « se souvient » de l’environnement dans lequel elle a été créée, même après la fin de l’exécution de cet environnement.

```javascript
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

let incrementer = createCounter();
console.log(incrementer()); // 1
console.log(incrementer()); // 2
console.log(incrementer()); // 3
```

Ici, la fonction renvoyée continue d’accéder à la variable `count`, bien que la fonction `createCounter` soit terminée. Cette capacité à capturer un contexte est très puissante, notamment pour créer des fonctions personnalisées ou gérer de la mémoire interne.

---

## À retenir

* La **portée globale** concerne les variables accessibles partout.
* La **portée locale** limite les variables à une fonction.
* La **portée de bloc** (avec `let` et `const`) restreint les variables à l’intérieur des accolades.
* Les **fermetures** permettent à une fonction de conserver l’accès aux variables de son environnement, même après la fin de celui-ci.

Comprendre ces notions est fondamental pour éviter les erreurs de logique et pour écrire du code clair et robuste.

---

⬅️ [Chapitre précédent : Les Paramètres](./c_Parametres.md)

➡️ [Chapitre suivant : Les Fonctions fléchées](./e_FonctionsFlechees.md)
