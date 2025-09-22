---
chapter: 7
section: a
title: Les Boucles
description: Les boucles sont des structures de contrôle qui permettent d'exécuter un bloc de code de façon répétée jusqu’à ce qu’une condition précise soit remplie. Elles sont essentielles pour automatiser des tâches récurrentes et parcourir des structures de données telles que les tableaux ou les chaînes de caractères.
---

# Les Boucles

En programmation, il est fréquent d’avoir besoin de répéter une même opération plusieurs fois. Les boucles sont justement conçues pour cela : elles permettent de demander à l’ordinateur de répéter une série d’instructions tant qu’une condition donnée est remplie. Elles évitent ainsi la répétition manuelle de lignes de code et rendent le programme plus clair et plus efficace.

Prenons un exemple simple. Sans boucle, on serait obligé d’écrire chaque instruction séparément :

```javascript
faireQqch(voiture[0]);
faireQqch(voiture[1]);
faireQqch(voiture[2]);
faireQqch(voiture[3]);
faireQqch(voiture[4]);
```

Avec une boucle, la même logique devient beaucoup plus concise et maintenable :

```javascript
for (let i = 0; i < voiture.length; i++) {
  faireQqch(voiture[i]);
}
```

Dans cet exemple, la variable `i` commence à zéro et augmente de un à chaque passage. La boucle s’exécute tant que la condition `i < voiture.length` est vraie. Cela permet de parcourir tous les éléments du tableau sans avoir à répéter les appels un par un.

Les boucles ne se limitent pas aux tableaux. Elles s’emploient dans toutes sortes de situations : effectuer une action un nombre déterminé de fois, parcourir des chaînes de caractères, vérifier des données, ou encore attendre qu’une certaine condition soit atteinte avant de poursuivre l’exécution du programme.

---

## À retenir

Les boucles sont une **structure de contrôle fondamentale**.
Elles permettent d’exécuter un même bloc de code plusieurs fois, en variant généralement la valeur d’une variable à chaque passage.
Grâce à elles, un programme devient à la fois plus court, plus lisible et plus puissant.

---

⬅️ [Chapitre précédent : Les Fonctions](../06_fonctions/d_Fonctions.md)

➡️ [Chapitre suivant : La Boucle For](./b_For.md)

