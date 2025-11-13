---
chapter: 7
section: d
title: La Boucle Do...While
description: La boucle do...while permet d’exécuter un bloc d’instructions au moins une fois, puis de répéter ce bloc tant que la condition spécifiée reste vraie. Contrairement à while, la condition est évaluée après l’exécution.
---

# La Boucle Do...While

La boucle **do...while** ressemble beaucoup à la boucle `while`, mais avec une différence essentielle : elle garantit que le bloc de code s’exécute **au moins une fois**, même si la condition est fausse dès le départ. Cela tient au fait que la condition est vérifiée seulement après l’exécution de l’instruction.

La syntaxe générale est la suivante :

```javascript
do {
  // instructions à exécuter
} while (condition);
```

## Exemple simple

Affichons les nombres de 0 à 9 en utilisant une boucle `do...while` :

```javascript
let i = 0;

do {
  console.log(i);
  i++;
} while (i < 10);
```

Dans cet exemple, la variable `i` est initialisée à 0. Le bloc s’exécute une première fois, puis la condition `i < 10` est évaluée. Tant qu’elle reste vraie, la boucle continue. Dès que `i` atteint 10, la boucle prend fin.

## Particularité du do...while

La différence avec la boucle `while` réside dans le moment de l’évaluation de la condition. Avec `while`, la condition est testée **avant** l’exécution, ce qui peut empêcher le bloc de s’exécuter si elle est fausse dès le départ. Avec `do...while`, le bloc s’exécute **au moins une fois**, quoi qu’il arrive, puis seulement la condition est testée.

---

## À retenir

La boucle **do...while** est utile lorsque l’on veut s’assurer qu’un bloc de code s’exécute au minimum une fois, même si la condition n’est pas remplie.
Elle s’apparente à la boucle `while`, mais son fonctionnement repose sur une évaluation différée de la condition.

---

⬅️ [Chapitre précédent : La Boucle While](./c_while.md)

➡️ [Chapitre suivant : Itérations Modernes](./e_iterations.md)
