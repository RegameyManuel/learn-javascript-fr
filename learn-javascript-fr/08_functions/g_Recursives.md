---
chapter: 8
section: g
title: Les Fonctions récursives
description: Une fonction récursive est une fonction qui s’appelle elle-même. Cette technique permet de résoudre des problèmes définis de manière répétitive ou hiérarchique.
---

# Les Fonctions récursives

Une **fonction récursive** est une fonction qui s’appelle elle-même au cours de son exécution.  
Cette technique est particulièrement adaptée pour résoudre des problèmes qui peuvent être découpés en sous-problèmes plus simples, semblables au problème initial.

En pratique, une fonction récursive doit toujours définir deux choses essentielles :  

1. **Le cas de base** : une condition qui met fin à la récursion.  
2. **L’appel récursif** : l’appel de la fonction sur une version réduite du problème.  

Sans cas de base, la fonction s’appellerait indéfiniment et provoquerait une erreur de débordement de pile.



## Exemple simple : le compte à rebours

```javascript
function compteARebours(n) {
  if (n <= 0) {
    console.log("Décollage !");
  } else {
    console.log(n);
    compteARebours(n - 1);
  }
}

compteARebours(5);
// 5
// 4
// 3
// 2
// 1
// Décollage !
```

Ici, le cas de base est atteint lorsque `n <= 0`.
Sinon, la fonction s’appelle elle-même avec une valeur réduite (`n - 1`).



## Exemple classique : factorielle

La factorielle d’un nombre `n` (notée `n!`) est définie ainsi :

* `0! = 1`
* `n! = n × (n-1)!` pour tout `n > 0`

Cette définition mathématique se prête parfaitement à une fonction récursive :

```javascript
function factorielle(n) {
  if (n === 0) {
    return 1; // cas de base
  } else {
    return n * factorielle(n - 1); // appel récursif
  }
}

console.log(factorielle(5)); // 120
```



## Exemple : parcourir une structure imbriquée

La récursion est très utile pour naviguer dans des structures de données arborescentes (objets imbriqués, dossiers, arbres, etc.).

```javascript
function afficherObj(obj) {
  for (let cle in obj) {
    if (typeof obj[cle] === "object") {
      afficherObj(obj[cle]); // appel récursif
    } else {
      console.log(cle + " : " + obj[cle]);
    }
  }
}

let utilisateur = {
  nom: "Alice",
  infos: {
    age: 30,
    adresse: {
      ville: "Paris",
      code: 75000
    }
  }
};

afficherObj(utilisateur);
// nom : Alice
// age : 30
// ville : Paris
// code : 75000
```



## Avantages et limites

La récursion est élégante et correspond souvent à la définition naturelle d’un problème.
Cependant, elle peut être moins performante que les boucles, car chaque appel consomme de la mémoire sur la pile d’exécution. Dans certains cas, il est préférable d’utiliser une version itérative.

---

## À retenir

Les fonctions récursives s’appellent elles-mêmes pour résoudre un problème en le divisant en sous-problèmes plus simples.
Elles nécessitent toujours un **cas de base** pour éviter les boucles infinies.
La récursion est puissante pour les problèmes hiérarchiques, mais doit être utilisée avec discernement afin d’éviter des problèmes de performance.

---

⬅️ [Chapitre précédent : Les Closures](./f_Closures.md)

➡️ [Chapitre suivant : Les Fonctions asynchrones](./h_Exercices)

