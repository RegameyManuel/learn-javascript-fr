---
chapter: 8
section: f
title: Les Closures
description: Une closure est une fonction qui se souvient du contexte dans lequel elle a été créée. Elle permet de conserver l’accès aux variables environnantes même après la fin de leur exécution.
---

# Les Closures

En JavaScript, une fonction ne vit pas isolée : elle conserve un lien avec l’environnement dans lequel elle a été créée. Cette propriété particulière s’appelle une **closure** (ou fermeture). Grâce à elle, une fonction peut se souvenir des variables de son contexte d’origine, même si ce contexte est terminé.



## Exemple simple

Prenons une fonction qui renvoie une autre fonction :

```javascript
function creerCompteur() {
  let compteur = 0;

  return function() {
    compteur++;
    return compteur;
  };
}

let incrementer = creerCompteur();

console.log(incrementer()); // 1
console.log(incrementer()); // 2
console.log(incrementer()); // 3
```

Ici, la variable `compteur` appartient normalement à la fonction `creerCompteur`. Pourtant, la fonction renvoyée continue d’y avoir accès, même après la fin de `creerCompteur`. C’est l’essence même d’une closure.



## Pourquoi est-ce utile ?

Les closures permettent de créer des fonctions **personnalisées** et **persistantes**.
Elles sont largement utilisées pour :

* **Protéger des variables internes** : les variables d’une closure ne sont pas accessibles directement de l’extérieur, ce qui crée une sorte d’« encapsulation ».
* **Créer des fonctions configurées** : une closure peut retenir une valeur et construire une fonction spécialisée.
* **Gérer l’état dans un environnement fonctionnel** : elles offrent un moyen élégant de mémoriser des données sans utiliser d’objets complexes.



## Exemple : fonction personnalisée

Imaginons une fonction qui fabrique des multiplicateurs :

```javascript
function fabriquerMultiplicateur(x) {
  return function(y) {
    return x * y;
  };
}

let doubler = fabriquerMultiplicateur(2);
let tripler = fabriquerMultiplicateur(3);

console.log(doubler(5)); // 10
console.log(tripler(5)); // 15
```

Chaque fonction produite garde en mémoire la valeur de `x` définie lors de sa création.



## Exemple : variables privées

Les closures sont aussi utiles pour simuler des **variables privées** en JavaScript :

```javascript
function creerBanque() {
  let solde = 0;

  return {
    deposer: function(montant) {
      solde += montant;
      return solde;
    },
    retirer: function(montant) {
      solde -= montant;
      return solde;
    },
    consulter: function() {
      return solde;
    }
  };
}

let monCompte = creerBanque();

console.log(monCompte.deposer(100)); // 100
console.log(monCompte.retirer(30));  // 70
console.log(monCompte.consulter());  // 70
```

Ici, la variable `solde` n’est pas accessible directement. Seules les fonctions internes y ont accès, ce qui garantit une meilleure sécurité des données.

---

## À retenir

Une **closure** est une fonction qui conserve l’accès à son environnement de création.
Elle permet de créer des fonctions spécialisées, de gérer un état persistant et de protéger des variables internes.
Les closures sont une des notions les plus puissantes et subtiles du langage JavaScript : elles combinent la souplesse des fonctions avec la mémoire d’un contexte.

---

⬅️ [Chapitre précédent : Les Fonctions fléchées](./e_FonctionsFlechees.md)

➡️ [Chapitre suivant : Les Fonctions récursives](./g_Recursives.md)
