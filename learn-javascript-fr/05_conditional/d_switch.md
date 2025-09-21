---
chapter: 5
section: d
title: Switch
description: Comprendre l’utilisation de l’instruction switch en JavaScript pour gérer plusieurs cas possibles de manière claire et lisible.
---

# L’instruction switch

L’instruction **`switch`** est une alternative à la succession de `if / else if / else`.  
Elle est particulièrement pratique lorsqu’il s’agit de comparer une même variable à plusieurs valeurs possibles.


## Syntaxe de base

```javascript
switch (expression) {
  case valeur1:
    // instructions si expression === valeur1
    break;
  case valeur2:
    // instructions si expression === valeur2
    break;
  default:
    // instructions si aucune valeur ne correspond
}
```

* L’expression placée après `switch` est évaluée.
* Chaque `case` est testé : si l’expression est strictement égale à la valeur indiquée, le bloc correspondant est exécuté.
* Le mot clé `break` permet de sortir du switch et d’éviter d’exécuter les blocs suivants.
* Le bloc `default` est optionnel et s’exécute si aucun des `case` ne correspond.


## Exemple

```javascript
let fruit = "banane";

switch (fruit) {
  case "pomme":
    console.log("C’est une pomme");
    break;
  case "banane":
    console.log("C’est une banane");
    break;
  case "orange":
    console.log("C’est une orange");
    break;
  default:
    console.log("Fruit inconnu");
}
```

Ici, la valeur `"banane"` correspond au deuxième `case`.
Le message `"C’est une banane"` est donc affiché.


## Exercice

1. Déclarez une variable `jour` avec la valeur `"lundi"`.
2. Utilisez un `switch` pour afficher :

   * `"Début de semaine"` si `jour` est `"lundi"`,
   * `"Milieu de semaine"` si `jour` est `"mercredi"`,
   * `"Fin de semaine"` si `jour` est `"vendredi"`,
   * `"Jour non reconnu"` dans les autres cas.

### Solution attendue

```javascript
let jour = "lundi";

switch (jour) {
  case "lundi":
    console.log("Début de semaine");
    break;
  case "mercredi":
    console.log("Milieu de semaine");
    break;
  case "vendredi":
    console.log("Fin de semaine");
    break;
  default:
    console.log("Jour non reconnu");
}
```

---

## À retenir

* L’instruction `switch` permet de tester une même expression contre plusieurs valeurs.
* Chaque `case` correspond à une valeur possible et doit être terminé par `break`.
* Le bloc `default` est optionnel et sert de solution de repli.

---

⬅️ [Chapitre précédent : Else](./c_else.md)
➡️ [Chapitre suivant : Comparaison](./e_Comparaison.md)

