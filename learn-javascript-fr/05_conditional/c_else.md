---
chapter: 5
section: c
title: L’instruction else
description: Comprendre comment utiliser l’instruction else pour exécuter une alternative lorsqu’une condition n’est pas remplie.
---

# L’instruction else

L’instruction `else` complète l’instruction `if`.  
Elle permet de définir un bloc de code qui sera exécuté lorsque la condition du `if` est fausse.  
Ainsi, on peut prévoir deux chemins différents : un si la condition est vraie, un autre si elle est fausse.


## Exemple simple

```javascript
let x = 5;

if (x > 10) {
  console.log("x est supérieur à 10");
} else {
  console.log("x est inférieur ou égal à 10");
}
```

Dans cet exemple, comme `x` vaut 5, la condition `x > 10` est fausse.
C’est donc le bloc `else` qui est exécuté, et le message `"x est inférieur ou égal à 10"` apparaît.


## else if
L'instruction `else`peut également être assortie d'un autre `if`, on parle dans ce cas d'un sinon si. Chaque condition va être testée à la suite l'une de l'autre. Dès lors que l'une d'entre elles sera évaluée à true, l'exécution du code se pousuivra dans le bloc de code correspondant et il en sera fini pour ce bloc. Dans ce cas, les conditions placées en dessous ne seront pas évaluées. Réécrivons l'exemple précédent en suivant cette logique du si/sinon si/sinon.

```javascript
let country = "France";

if (country === "Espagne") {
  console.log("Ola");       // ne s'exécute pas
} else if (country === "France") {
  console.log("Bonjour");   // s'exécute
} else if (country === "Allemagne") {
  console.log("Guten Tag"); // ne s'exécute pas
} else {
  console.log("Hello"); // ne s'exécute pas
}
```


---

## À retenir

* L’instruction `else` définit un bloc de code exécuté si la condition du `if` est fausse.
* Avec `if/else`, on couvre toujours deux cas possibles : condition vraie ou condition fausse.
* C’est la base des tests binaires en programmation.

---

⬅️ [Chapitre précédent : If](./b_if.md)

➡️ [Chapitre suivant : Switch](./d_switch.md)
