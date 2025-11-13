---
chapter: 7
section: c
title: La Boucle While
description: La boucle while exécute un bloc de code tant qu’une condition donnée est vraie. Elle est particulièrement adaptée aux situations où l’on ne connaît pas à l’avance le nombre d’itérations nécessaires.
---

# La Boucle While

La boucle **while** est l’une des formes les plus simples d’itération en JavaScript. Elle repose sur une idée fondamentale : tant qu’une condition reste vraie, le bloc d’instructions continue de s’exécuter. Dès que la condition devient fausse, la boucle s’interrompt et l’exécution du programme reprend normalement.

La syntaxe générale est la suivante :

```javascript
while (condition) {
  // instructions à exécuter tant que la condition est vraie
}
```

Ici, la condition est évaluée **avant chaque itération**. Si elle est fausse dès le départ, la boucle ne s’exécutera jamais.

## Exemple simple

Imaginons que l’on souhaite afficher une série de nombres. Nous pouvons utiliser une boucle `while` pour incrémenter une variable jusqu’à atteindre une limite définie :

```javascript
let i = 0;
let texte = "";

while (i < 5) {
  texte += "Le nombre est " + i + "\n";
  i++;
}

console.log(texte);
```

Dans cet exemple, la variable `i` commence à 0. Tant que `i` est inférieure à 5, le message est ajouté au texte, puis `i` est augmenté de 1. La boucle s’arrête automatiquement lorsque `i` atteint 5.

## Attention aux boucles infinies

Une boucle `while` doit toujours comporter une évolution de la variable testée, sans quoi la condition resterait indéfiniment vraie. On parle alors de **boucle infinie** : le programme reste bloqué, exécutant le même code sans fin. Pour les éviter, il est crucial de s’assurer que la condition deviendra fausse à un moment donné.

---

## À retenir

La boucle **while** est utile lorsque l’on ne connaît pas à l’avance le nombre d’itérations nécessaires.
Elle répète un bloc tant qu’une condition est vraie, et s’arrête dès que celle-ci devient fausse.
Il faut veiller à éviter les conditions qui ne changent jamais, afin de ne pas créer de boucles infinies.

---

⬅️ [Chapitre précédent : La Boucle For](./b_For.md)

➡️ [Chapitre suivant : La Boucle Do...While](./d_DoWhile.md)
